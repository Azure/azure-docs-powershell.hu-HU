---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Set-AzSqlDatabaseAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAudit.md
ms.openlocfilehash: e13e97bd9f636de68344f83b600e440252431a22
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194511"
---
# <span data-ttu-id="f1c99-101">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="f1c99-101">Set-AzSqlDatabaseAudit</span></span>

## <span data-ttu-id="f1c99-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f1c99-102">SYNOPSIS</span></span>
<span data-ttu-id="f1c99-103">Az Azure SQL-adatbázisok naplózási beállításainak módosítása</span><span class="sxs-lookup"><span data-stu-id="f1c99-103">Changes the auditing settings for an Azure SQL database.</span></span>

## <span data-ttu-id="f1c99-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f1c99-104">SYNTAX</span></span>

### <span data-ttu-id="f1c99-105">DatabaseParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f1c99-105">DatabaseParameterSet (Default)</span></span>
```
Set-AzSqlDatabaseAudit [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-EventHubTargetState <String>]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1c99-106">DatabaseObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1c99-106">DatabaseObjectParameterSet</span></span>
```
Set-AzSqlDatabaseAudit [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-EventHubTargetState <String>]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] -DatabaseObject <AzureSqlDatabaseModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1c99-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f1c99-107">DESCRIPTION</span></span>
<span data-ttu-id="f1c99-108">A **set-AzSqlDatabaseAudit** parancsmag egy Azure SQL-adatbázis naplózási beállításait módosítja.</span><span class="sxs-lookup"><span data-stu-id="f1c99-108">The **Set-AzSqlDatabaseAudit** cmdlet changes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="f1c99-109">A parancsmag használatához a *ResourceGroupName* , a *kiszolgálónév* és a *databasename* paraméterrel keresse meg az adatbázist.</span><span class="sxs-lookup"><span data-stu-id="f1c99-109">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="f1c99-110">Ha a blob-tároló a naplók rendeltetése, akkor a *StorageAccountResourceId* paraméterrel határozhatja meg a naplók tárolási fiókját és a *StorageKeyType* paramétert a tárolási kulcsok meghatározásához.</span><span class="sxs-lookup"><span data-stu-id="f1c99-110">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="f1c99-111">A naplók adatmegőrzését úgy is megadhatja, hogy az *RetentionInDays* paraméter értékét adja meg a naplók időszakának meghatározásához.</span><span class="sxs-lookup"><span data-stu-id="f1c99-111">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

## <span data-ttu-id="f1c99-112">Példák</span><span class="sxs-lookup"><span data-stu-id="f1c99-112">EXAMPLES</span></span>

### <span data-ttu-id="f1c99-113">1. példa: a blob-tároló naplózási házirendjének engedélyezése Azure SQL-adatbázisokban</span><span class="sxs-lookup"><span data-stu-id="f1c99-113">Example 1: Enable the blob storage auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorageTargetState Enabled  -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### <span data-ttu-id="f1c99-114">2. példa: az Azure SQL-adatbázisok blob-tároló naplózási házirendjének letiltása</span><span class="sxs-lookup"><span data-stu-id="f1c99-114">Example 2: Disable the blob storage auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="f1c99-115">Példa 3: a blob-tároló naplózási házirendjének engedélyezése az Azure SQL-adatbázisokban speciális szűréssel a T-SQL predikátum használatával</span><span class="sxs-lookup"><span data-stu-id="f1c99-115">Example 3: Enable the blob storage auditing policy of an Azure SQL database with advanced filtering using a T-SQL predicate</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -PredicateExpression "statement <> 'select 1'" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### <span data-ttu-id="f1c99-116">4. példa: a speciális szűrési beállítás eltávolítása egy Azure SQL-adatbázis naplózási házirendjéből</span><span class="sxs-lookup"><span data-stu-id="f1c99-116">Example 4: Remove the advanced filtering setting from the auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -PredicateExpression ""
```

### <span data-ttu-id="f1c99-117">Példa 5: az Azure SQL-adatbázisok esemény-központi naplózási házirendjének engedélyezése</span><span class="sxs-lookup"><span data-stu-id="f1c99-117">Example 5: Enable the event hub auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId"
```

### <span data-ttu-id="f1c99-118">Példa 6: az Azure SQL-adatbázisok esemény-központi naplózási házirendjének letiltása</span><span class="sxs-lookup"><span data-stu-id="f1c99-118">Example 6: Disable the event hub auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -EventHubTargetState Disabled
```

### <span data-ttu-id="f1c99-119">7. példa: az Azure SQL-adatbázisok naplózási Analytics-naplózási házirendjének engedélyezése</span><span class="sxs-lookup"><span data-stu-id="f1c99-119">Example 7: Enable the log analytics auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="f1c99-120">8. példa: az Azure SQL-adatbázisok naplózási Analytics-naplózási házirendjének letiltása</span><span class="sxs-lookup"><span data-stu-id="f1c99-120">Example 8: Disable the log analytics auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="f1c99-121">9. példa: az Azure SQL-adatbázisok naplózási házirendjének letiltása a csővezetéken keresztül</span><span class="sxs-lookup"><span data-stu-id="f1c99-121">Example 9: Disable, through pipeline, the log analytics auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Set-AzSqlDatabaseAudit -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="f1c99-122">10 példa: tiltsa le az Azure SQL-adatbázisok naplózási rekordjainak blob-tárterületre való küldését, és engedélyezze a naplózást az Analytics szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="f1c99-122">Example 10: Disable sending audit records of an Azure SQL database to blob storage, and enable sending them to log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalyticsTargetState Enabled  -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="f1c99-123">11. példa: engedélyezze az Azure SQL-adatbázisok naplózási rekordjainak küldését a blob-tároló, az esemény-hub és a log Analytics segítségével.</span><span class="sxs-lookup"><span data-stu-id="f1c99-123">Example 11: Enable sending audit records of an Azure SQL database to blob storage, event hub and log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId" -LogAnalyticsTargetState Enabled  -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

## <span data-ttu-id="f1c99-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f1c99-124">PARAMETERS</span></span>

### <span data-ttu-id="f1c99-125">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="f1c99-125">-AuditAction</span></span>
<span data-ttu-id="f1c99-126">A naplózási műveletek halmaza.</span><span class="sxs-lookup"><span data-stu-id="f1c99-126">The set of audit actions.</span></span>  
<span data-ttu-id="f1c99-127">A naplózandó támogatott műveletek a következők:</span><span class="sxs-lookup"><span data-stu-id="f1c99-127">The supported actions to audit are:</span></span>  
<span data-ttu-id="f1c99-128">Válassza</span><span class="sxs-lookup"><span data-stu-id="f1c99-128">SELECT</span></span>  
<span data-ttu-id="f1c99-129">FRISSÍTÉS</span><span class="sxs-lookup"><span data-stu-id="f1c99-129">UPDATE</span></span>  
<span data-ttu-id="f1c99-130">BESZÚRÁSA</span><span class="sxs-lookup"><span data-stu-id="f1c99-130">INSERT</span></span>  
<span data-ttu-id="f1c99-131">TÖRLÉSE</span><span class="sxs-lookup"><span data-stu-id="f1c99-131">DELETE</span></span>  
<span data-ttu-id="f1c99-132">VÉGREHAJTÁSA</span><span class="sxs-lookup"><span data-stu-id="f1c99-132">EXECUTE</span></span>  
<span data-ttu-id="f1c99-133">KAP</span><span class="sxs-lookup"><span data-stu-id="f1c99-133">RECEIVE</span></span>  
<span data-ttu-id="f1c99-134">HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f1c99-134">REFERENCES</span></span>  
<span data-ttu-id="f1c99-135">A naplózandó műveletek meghatározására szolgáló általános űrlap: [művelet] ON [Object] BY [Principal] Ne feledje, hogy az [objektum] a fenti formátumban hivatkozhat egy objektumra, például táblázatra, nézetre vagy tárolt eljárásra, illetve egész adatbázisra vagy sémára.</span><span class="sxs-lookup"><span data-stu-id="f1c99-135">The general form for defining an action to be audited is: [action] ON [object] BY [principal] Note that [object] in the above format can refer to an object like a table, view, or stored procedure, or an entire database or schema.</span></span> <span data-ttu-id="f1c99-136">Az utóbbi esetekben az Forms DATABASE:: [dbname] és a SCHEMA:: [SchemaName] használatban van.</span><span class="sxs-lookup"><span data-stu-id="f1c99-136">For the latter cases, the forms DATABASE::[dbname] and SCHEMA::[schemaname] are used, respectively.</span></span>
<span data-ttu-id="f1c99-137">Példa:</span><span class="sxs-lookup"><span data-stu-id="f1c99-137">For example:</span></span>  
<span data-ttu-id="f1c99-138">Válassza a dbo. Táblanév nyilvánosak szerint lehetőséget</span><span class="sxs-lookup"><span data-stu-id="f1c99-138">SELECT on dbo.myTable by public</span></span>  
<span data-ttu-id="f1c99-139">Válassza az adatbázis: myDatabase nyilvánosak szerint lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="f1c99-139">SELECT on DATABASE::myDatabase by public</span></span>  
<span data-ttu-id="f1c99-140">SELECT on SCHEMA:: mySchema by Public</span><span class="sxs-lookup"><span data-stu-id="f1c99-140">SELECT on SCHEMA::mySchema by public</span></span>  
<span data-ttu-id="f1c99-141">További információ: https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions .</span><span class="sxs-lookup"><span data-stu-id="f1c99-141">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions.</span></span>

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

### <span data-ttu-id="f1c99-142">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="f1c99-142">-AuditActionGroup</span></span>
<span data-ttu-id="f1c99-143">A használni kívánt műveleti csoportok a következő kombinációk: Ez a művelet naplózza az adatbázissal végzett összes lekérdezést és tárolt eljárást, valamint a sikeres és sikertelen bejelentkezéseket:</span><span class="sxs-lookup"><span data-stu-id="f1c99-143">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="f1c99-144">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="f1c99-144">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="f1c99-145">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="f1c99-145">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="f1c99-146">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="f1c99-146">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  
<span data-ttu-id="f1c99-147">Ez a fenti kombináció egyben az alapértelmezés szerint konfigurált halmaz.</span><span class="sxs-lookup"><span data-stu-id="f1c99-147">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="f1c99-148">Ezek a csoportok az adatbázissal szemben végrehajtott összes SQL-utasítást és tárolt eljárást lefoglalják, és nem használhatók együtt más csoportokkal, mert ez a művelet duplikálja a naplókat.</span><span class="sxs-lookup"><span data-stu-id="f1c99-148">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="f1c99-149">További információ: https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="f1c99-149">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]
Parameter Sets: (All)
Aliases:
Accepted values: BATCH_STARTED_GROUP, BATCH_COMPLETED_GROUP, APPLICATION_ROLE_CHANGE_PASSWORD_GROUP, BACKUP_RESTORE_GROUP, DATABASE_LOGOUT_GROUP, DATABASE_OBJECT_CHANGE_GROUP, DATABASE_OBJECT_OWNERSHIP_CHANGE_GROUP, DATABASE_OBJECT_PERMISSION_CHANGE_GROUP, DATABASE_OPERATION_GROUP, DATABASE_PERMISSION_CHANGE_GROUP, DATABASE_PRINCIPAL_CHANGE_GROUP, DATABASE_PRINCIPAL_IMPERSONATION_GROUP, DATABASE_ROLE_MEMBER_CHANGE_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, SCHEMA_OBJECT_ACCESS_GROUP, SCHEMA_OBJECT_CHANGE_GROUP, SCHEMA_OBJECT_OWNERSHIP_CHANGE_GROUP, SCHEMA_OBJECT_PERMISSION_CHANGE_GROUP, SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, USER_CHANGE_PASSWORD_GROUP

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1c99-150">-BlobStorageTargetState</span><span class="sxs-lookup"><span data-stu-id="f1c99-150">-BlobStorageTargetState</span></span>
<span data-ttu-id="f1c99-151">Azt jelzi, hogy a blob-tároló a rekordok naplózására szolgáló cél-e.</span><span class="sxs-lookup"><span data-stu-id="f1c99-151">Indicates whether blob storage is a destination for audit records.</span></span>

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

### <span data-ttu-id="f1c99-152">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f1c99-152">-DatabaseName</span></span>
<span data-ttu-id="f1c99-153">SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="f1c99-153">SQL Database name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1c99-154">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="f1c99-154">-DatabaseObject</span></span>
<span data-ttu-id="f1c99-155">Az adatbázis-objektum a naplózási házirend kezeléséhez.</span><span class="sxs-lookup"><span data-stu-id="f1c99-155">The database object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: DatabaseObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f1c99-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1c99-156">-DefaultProfile</span></span>
<span data-ttu-id="f1c99-157">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f1c99-157">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1c99-158">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="f1c99-158">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="f1c99-159">Az esemény-hub engedélyezési szabályának erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="f1c99-159">The resource Id for the event hub authorization rule</span></span>

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

### <span data-ttu-id="f1c99-160">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="f1c99-160">-EventHubName</span></span>
<span data-ttu-id="f1c99-161">Az esemény központja neve.</span><span class="sxs-lookup"><span data-stu-id="f1c99-161">The name of the event hub.</span></span> <span data-ttu-id="f1c99-162">Ha a EventHubAuthorizationRuleResourceId megadásakor nincs megadva, az alapértelmezett esemény hub lesz kiválasztva.</span><span class="sxs-lookup"><span data-stu-id="f1c99-162">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

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

### <span data-ttu-id="f1c99-163">-EventHubTargetState</span><span class="sxs-lookup"><span data-stu-id="f1c99-163">-EventHubTargetState</span></span>
<span data-ttu-id="f1c99-164">Azt jelzi, hogy az esemény központja a rekordok naplózásának a rendeltetése.</span><span class="sxs-lookup"><span data-stu-id="f1c99-164">Indicates whether event hub is a destination for audit records.</span></span>

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

### <span data-ttu-id="f1c99-165">-LogAnalyticsTargetState</span><span class="sxs-lookup"><span data-stu-id="f1c99-165">-LogAnalyticsTargetState</span></span>
<span data-ttu-id="f1c99-166">Azt jelzi, hogy a napló-elemzés a rekordok naplózási célja-e.</span><span class="sxs-lookup"><span data-stu-id="f1c99-166">Indicates whether log analytics is a destination for audit records.</span></span>

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

### <span data-ttu-id="f1c99-167">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f1c99-167">-PassThru</span></span>
<span data-ttu-id="f1c99-168">Azt adja meg, hogy a naplózási házirendet a parancsmag-végrehajtás végén szeretné-e kivenni.</span><span class="sxs-lookup"><span data-stu-id="f1c99-168">Specifies whether to output the auditing policy at end of cmdlet execution</span></span>

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

### <span data-ttu-id="f1c99-169">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="f1c99-169">-PredicateExpression</span></span>
<span data-ttu-id="f1c99-170">A naplók szűréséhez használt T-SQL predikátum (WHERE záradék).</span><span class="sxs-lookup"><span data-stu-id="f1c99-170">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="f1c99-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1c99-171">-ResourceGroupName</span></span>
<span data-ttu-id="f1c99-172">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f1c99-172">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1c99-173">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="f1c99-173">-RetentionInDays</span></span>
<span data-ttu-id="f1c99-174">A naplók retenciós napjainak száma.</span><span class="sxs-lookup"><span data-stu-id="f1c99-174">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="f1c99-175">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="f1c99-175">-ServerName</span></span>
<span data-ttu-id="f1c99-176">SQL-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="f1c99-176">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1c99-177">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="f1c99-177">-StorageAccountResourceId</span></span>
<span data-ttu-id="f1c99-178">A tárolási fiók erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="f1c99-178">The storage account resource id</span></span>

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

### <span data-ttu-id="f1c99-179">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="f1c99-179">-StorageKeyType</span></span>
<span data-ttu-id="f1c99-180">Itt adhatja meg, hogy a tárterület-hozzáférési kulcsok közül melyik használható.</span><span class="sxs-lookup"><span data-stu-id="f1c99-180">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="f1c99-181">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="f1c99-181">-WorkspaceResourceId</span></span>
<span data-ttu-id="f1c99-182">A napló Analytics-munkaterületének erőforrás-azonosítója (log Analytics-munkaterületen), amelybe naplókat szeretne küldeni.</span><span class="sxs-lookup"><span data-stu-id="f1c99-182">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Audit Logs.</span></span> <span data-ttu-id="f1c99-183">Példa:/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span><span class="sxs-lookup"><span data-stu-id="f1c99-183">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

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

### <span data-ttu-id="f1c99-184">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f1c99-184">-Confirm</span></span>
<span data-ttu-id="f1c99-185">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f1c99-185">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1c99-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1c99-186">-WhatIf</span></span>
<span data-ttu-id="f1c99-187">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f1c99-187">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f1c99-188">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f1c99-188">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1c99-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1c99-189">CommonParameters</span></span>
<span data-ttu-id="f1c99-190">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f1c99-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1c99-191">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f1c99-191">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1c99-192">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f1c99-192">INPUTS</span></span>

### <span data-ttu-id="f1c99-193">System. String</span><span class="sxs-lookup"><span data-stu-id="f1c99-193">System.String</span></span>

### <span data-ttu-id="f1c99-194">Microsoft. Azure. Command. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="f1c99-194">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="f1c99-195">Microsoft. Azure. Command. SQL. könyvvizsgálat. Model. AuditActionGroups []</span><span class="sxs-lookup"><span data-stu-id="f1c99-195">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span></span>

### <span data-ttu-id="f1c99-196">System. string []</span><span class="sxs-lookup"><span data-stu-id="f1c99-196">System.String[]</span></span>

### <span data-ttu-id="f1c99-197">System. GUID</span><span class="sxs-lookup"><span data-stu-id="f1c99-197">System.Guid</span></span>

### <span data-ttu-id="f1c99-198">System. null ' 1 [[System. UInt32, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f1c99-198">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="f1c99-199">Microsoft. Azure. Command. SQL. könyvvizsgálat. Model. DatabaseAuditModel</span><span class="sxs-lookup"><span data-stu-id="f1c99-199">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseAuditModel</span></span>

## <span data-ttu-id="f1c99-200">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f1c99-200">OUTPUTS</span></span>

### <span data-ttu-id="f1c99-201">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f1c99-201">System.Boolean</span></span>

## <span data-ttu-id="f1c99-202">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f1c99-202">NOTES</span></span>

## <span data-ttu-id="f1c99-203">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f1c99-203">RELATED LINKS</span></span>