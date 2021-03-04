---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: https://docs.microsoft.com/powershell/module/az.sql/Set-AzSqlDatabaseAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAudit.md
ms.openlocfilehash: 6e3c5c935f6703f5c4f29b2a4ae793fc48e9b16f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940881"
---
# <span data-ttu-id="52c2f-101">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="52c2f-101">Set-AzSqlDatabaseAudit</span></span>

## <span data-ttu-id="52c2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52c2f-102">SYNOPSIS</span></span>
<span data-ttu-id="52c2f-103">Egy Azure SQL-adatbázis naplózási beállításait módosítja.</span><span class="sxs-lookup"><span data-stu-id="52c2f-103">Changes the auditing settings for an Azure SQL database.</span></span>

## <span data-ttu-id="52c2f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="52c2f-104">SYNTAX</span></span>

### <span data-ttu-id="52c2f-105">DatabaseParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="52c2f-105">DatabaseParameterSet (Default)</span></span>
```
Set-AzSqlDatabaseAudit [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-EventHubTargetState <String>]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52c2f-106">DatabaseObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="52c2f-106">DatabaseObjectParameterSet</span></span>
```
Set-AzSqlDatabaseAudit [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-EventHubTargetState <String>]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] -DatabaseObject <AzureSqlDatabaseModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52c2f-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="52c2f-107">DESCRIPTION</span></span>
<span data-ttu-id="52c2f-108">A **Set-AzSqlDatabaseAudit** parancsmag megváltoztatja egy Azure SQL-adatbázis naplózási beállításait.</span><span class="sxs-lookup"><span data-stu-id="52c2f-108">The **Set-AzSqlDatabaseAudit** cmdlet changes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="52c2f-109">A parancsmagot a *ResourceGroupName,* *a ServerName* és a *DatabaseName* paraméter használatával azonosíthatja az adatbázist.</span><span class="sxs-lookup"><span data-stu-id="52c2f-109">To use the cmdlet, use the *ResourceGroupName*, *ServerName*, and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="52c2f-110">Ha a blobtár a naplók célhelye, a *StorageAccountResourceId* paramétert megadva határozza meg a naplók tárfiókját és a *StorageKeyType* paramétert a tárkulcsok meghatározásához.</span><span class="sxs-lookup"><span data-stu-id="52c2f-110">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="52c2f-111">A naplók megőrzési időszakának meghatározásához a *RetentionInDays* paraméter értékét megadva is megadhatja a naplók időszakát.</span><span class="sxs-lookup"><span data-stu-id="52c2f-111">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

## <span data-ttu-id="52c2f-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="52c2f-112">EXAMPLES</span></span>

### <span data-ttu-id="52c2f-113">1. példa: Azure SQL-adatbázis blobtárhely-naplózási házirendének engedélyezése</span><span class="sxs-lookup"><span data-stu-id="52c2f-113">Example 1: Enable the blob storage auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorageTargetState Enabled  -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### <span data-ttu-id="52c2f-114">2. példa: Azure SQL-adatbázis blobtárhely-naplózási házirendének letiltása</span><span class="sxs-lookup"><span data-stu-id="52c2f-114">Example 2: Disable the blob storage auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="52c2f-115">3. példa: Egy Azure SQL-adatbázis blobtárhely-naplózási házirendének engedélyezése T-SQL predikátum használatával való szűréssel</span><span class="sxs-lookup"><span data-stu-id="52c2f-115">Example 3: Enable the blob storage auditing policy of an Azure SQL database with filtering using a T-SQL predicate</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -PredicateExpression "schema_name <> 'sys''" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### <span data-ttu-id="52c2f-116">4. példa: Azure SQL-adatbázis naplózási házirendje szűrésének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="52c2f-116">Example 4: Remove the filtering from the auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -PredicateExpression ""
```

### <span data-ttu-id="52c2f-117">5. példa: Azure SQL-adatbázis eseményközpont-naplózási házirendének engedélyezése</span><span class="sxs-lookup"><span data-stu-id="52c2f-117">Example 5: Enable the event hub auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId"
```

### <span data-ttu-id="52c2f-118">6. példa: Azure SQL-adatbázis eseményközpont-naplózási házirendének letiltása</span><span class="sxs-lookup"><span data-stu-id="52c2f-118">Example 6: Disable the event hub auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -EventHubTargetState Disabled
```

### <span data-ttu-id="52c2f-119">7. példa: Azure SQL-adatbázis naplóelemzési házirendének engedélyezése</span><span class="sxs-lookup"><span data-stu-id="52c2f-119">Example 7: Enable the log analytics auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="52c2f-120">8. példa: Azure SQL-adatbázis naplóelemzési házirendének letiltása</span><span class="sxs-lookup"><span data-stu-id="52c2f-120">Example 8: Disable the log analytics auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="52c2f-121">9. példa: Azure SQL-adatbázis naplóelemzési házirendének letiltása folyamaton keresztül</span><span class="sxs-lookup"><span data-stu-id="52c2f-121">Example 9: Disable, through pipeline, the log analytics auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Set-AzSqlDatabaseAudit -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="52c2f-122">10. példa: Tiltsa le egy Azure SQL-adatbázis naplórekordjainak blobtárolóba küldését, és engedélyezze a naplóelemzéshez való küldést.</span><span class="sxs-lookup"><span data-stu-id="52c2f-122">Example 10: Disable sending audit records of an Azure SQL database to blob storage, and enable sending them to log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalyticsTargetState Enabled  -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="52c2f-123">11. példa: Azure SQL-adatbázis naplórekordjainak blobtárolóba, eseményközpontba és naplóelemzésbe való küldésének engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="52c2f-123">Example 11: Enable sending audit records of an Azure SQL database to blob storage, event hub and log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId" -LogAnalyticsTargetState Enabled  -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

## <span data-ttu-id="52c2f-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="52c2f-124">PARAMETERS</span></span>

### <span data-ttu-id="52c2f-125">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="52c2f-125">-AuditAction</span></span>
<span data-ttu-id="52c2f-126">A naplózási műveletek halmaza.</span><span class="sxs-lookup"><span data-stu-id="52c2f-126">The set of audit actions.</span></span>  
<span data-ttu-id="52c2f-127">A támogatott naplóműveletek a következőek:</span><span class="sxs-lookup"><span data-stu-id="52c2f-127">The supported actions to audit are:</span></span>  
<span data-ttu-id="52c2f-128">SELECT</span><span class="sxs-lookup"><span data-stu-id="52c2f-128">SELECT</span></span>  
<span data-ttu-id="52c2f-129">FRISSÍTÉS</span><span class="sxs-lookup"><span data-stu-id="52c2f-129">UPDATE</span></span>  
<span data-ttu-id="52c2f-130">INSERT</span><span class="sxs-lookup"><span data-stu-id="52c2f-130">INSERT</span></span>  
<span data-ttu-id="52c2f-131">DELETE</span><span class="sxs-lookup"><span data-stu-id="52c2f-131">DELETE</span></span>  
<span data-ttu-id="52c2f-132">EXECUTE</span><span class="sxs-lookup"><span data-stu-id="52c2f-132">EXECUTE</span></span>  
<span data-ttu-id="52c2f-133">RECEIVE</span><span class="sxs-lookup"><span data-stu-id="52c2f-133">RECEIVE</span></span>  
<span data-ttu-id="52c2f-134">HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="52c2f-134">REFERENCES</span></span>  
<span data-ttu-id="52c2f-135">A naplózó művelet meghatározásának általános formája a következő: [művelet] ON [objektum] BY [principal] Megjegyzés: a fenti formátumban az [objektum] hivatkozhat objektumra, például táblázatra, nézetre vagy tárolt eljárásra, illetve egy teljes adatbázisra vagy sémára.</span><span class="sxs-lookup"><span data-stu-id="52c2f-135">The general form for defining an action to be audited is: [action] ON [object] BY [principal] Note that [object] in the above format can refer to an object like a table, view, or stored procedure, or an entire database or schema.</span></span> <span data-ttu-id="52c2f-136">Az utóbbi esetekben a DATABASE::[dbname] és a SCHEMA::[sémanév] űrlapot használja a rendszer.</span><span class="sxs-lookup"><span data-stu-id="52c2f-136">For the latter cases, the forms DATABASE::[dbname] and SCHEMA::[schemaname] are used, respectively.</span></span>
<span data-ttu-id="52c2f-137">Például:</span><span class="sxs-lookup"><span data-stu-id="52c2f-137">For example:</span></span>  
<span data-ttu-id="52c2f-138">SELECT on dbo.myTable by public</span><span class="sxs-lookup"><span data-stu-id="52c2f-138">SELECT on dbo.myTable by public</span></span>  
<span data-ttu-id="52c2f-139">SELECT on DATABASE::myDatabase by public</span><span class="sxs-lookup"><span data-stu-id="52c2f-139">SELECT on DATABASE::myDatabase by public</span></span>  
<span data-ttu-id="52c2f-140">SELECT on SCHEMA::mySchema by public</span><span class="sxs-lookup"><span data-stu-id="52c2f-140">SELECT on SCHEMA::mySchema by public</span></span>  
<span data-ttu-id="52c2f-141">További információ: https://docs.microsoft.com/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions .</span><span class="sxs-lookup"><span data-stu-id="52c2f-141">For more information, see https://docs.microsoft.com/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions.</span></span>

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

### <span data-ttu-id="52c2f-142">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="52c2f-142">-AuditActionGroup</span></span>
<span data-ttu-id="52c2f-143">A javasolt műveletcsoportok a következő kombinációk – ez naplóz minden lekérdezést és tárolt eljárást az adatbázison, valamint a sikeres és sikertelen bejelentkezéseket:</span><span class="sxs-lookup"><span data-stu-id="52c2f-143">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="52c2f-144">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="52c2f-144">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="52c2f-145">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="52c2f-145">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="52c2f-146">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="52c2f-146">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  
<span data-ttu-id="52c2f-147">Ez a fenti kombináció az alapértelmezés szerint konfigurált halmaz is.</span><span class="sxs-lookup"><span data-stu-id="52c2f-147">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="52c2f-148">Ezek a csoportok az adatbázison végrehajtott összes SQL-utasításra és tárolt eljárásra vonatkoznak, és nem használhatók más csoportokkal együtt, mert ez ismétlődő naplókat eredményez.</span><span class="sxs-lookup"><span data-stu-id="52c2f-148">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="52c2f-149">További információ: https://docs.microsoft.com/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="52c2f-149">For more information, see https://docs.microsoft.com/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="52c2f-150">-BlobstorageTargetState</span><span class="sxs-lookup"><span data-stu-id="52c2f-150">-BlobStorageTargetState</span></span>
<span data-ttu-id="52c2f-151">Azt jelzi, hogy a blobtároló a naplórekordok célhelyét jelenti-e.</span><span class="sxs-lookup"><span data-stu-id="52c2f-151">Indicates whether blob storage is a destination for audit records.</span></span>

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

### <span data-ttu-id="52c2f-152">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="52c2f-152">-DatabaseName</span></span>
<span data-ttu-id="52c2f-153">SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="52c2f-153">SQL Database name.</span></span>

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

### <span data-ttu-id="52c2f-154">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="52c2f-154">-DatabaseObject</span></span>
<span data-ttu-id="52c2f-155">A naplózási házirendet kezelő adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="52c2f-155">The database object to manage its audit policy.</span></span>

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

### <span data-ttu-id="52c2f-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52c2f-156">-DefaultProfile</span></span>
<span data-ttu-id="52c2f-157">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="52c2f-157">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52c2f-158">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="52c2f-158">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="52c2f-159">Az eseményközpont engedélyezési szabályának erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="52c2f-159">The resource Id for the event hub authorization rule</span></span>

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

### <span data-ttu-id="52c2f-160">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="52c2f-160">-EventHubName</span></span>
<span data-ttu-id="52c2f-161">Az eseményközpont neve.</span><span class="sxs-lookup"><span data-stu-id="52c2f-161">The name of the event hub.</span></span> <span data-ttu-id="52c2f-162">Ha az EventHubAuthorizationRuleResourceId megadva nincs megadva, az alapértelmezett eseményközpont lesz kiválasztva.</span><span class="sxs-lookup"><span data-stu-id="52c2f-162">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

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

### <span data-ttu-id="52c2f-163">-EventHubTargetState</span><span class="sxs-lookup"><span data-stu-id="52c2f-163">-EventHubTargetState</span></span>
<span data-ttu-id="52c2f-164">Azt jelzi, hogy az eseményközpont a naplórekordok célhelyének-e.</span><span class="sxs-lookup"><span data-stu-id="52c2f-164">Indicates whether event hub is a destination for audit records.</span></span>

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

### <span data-ttu-id="52c2f-165">-LogAnalyticsTargetState</span><span class="sxs-lookup"><span data-stu-id="52c2f-165">-LogAnalyticsTargetState</span></span>
<span data-ttu-id="52c2f-166">Azt jelzi, hogy a naplóelemzés a naplórekordok célhelyének-e.</span><span class="sxs-lookup"><span data-stu-id="52c2f-166">Indicates whether log analytics is a destination for audit records.</span></span>

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

### <span data-ttu-id="52c2f-167">-PassThru</span><span class="sxs-lookup"><span data-stu-id="52c2f-167">-PassThru</span></span>
<span data-ttu-id="52c2f-168">Megadja, hogy kimenetként adja-e meg a naplózási házirendet a parancsmag végrehajtásának végén.</span><span class="sxs-lookup"><span data-stu-id="52c2f-168">Specifies whether to output the auditing policy at end of cmdlet execution</span></span>

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

### <span data-ttu-id="52c2f-169">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="52c2f-169">-PredicateExpression</span></span>
<span data-ttu-id="52c2f-170">A naplók szűréséhez használt T-SQL predikátum (WHERE záradék).</span><span class="sxs-lookup"><span data-stu-id="52c2f-170">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="52c2f-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52c2f-171">-ResourceGroupName</span></span>
<span data-ttu-id="52c2f-172">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="52c2f-172">The name of the resource group.</span></span>

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

### <span data-ttu-id="52c2f-173">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="52c2f-173">-RetentionInDays</span></span>
<span data-ttu-id="52c2f-174">A naplók adatmegőrzési napjainak száma.</span><span class="sxs-lookup"><span data-stu-id="52c2f-174">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="52c2f-175">-ServerName</span><span class="sxs-lookup"><span data-stu-id="52c2f-175">-ServerName</span></span>
<span data-ttu-id="52c2f-176">SQL-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="52c2f-176">SQL server name.</span></span>

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

### <span data-ttu-id="52c2f-177">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="52c2f-177">-StorageAccountResourceId</span></span>
<span data-ttu-id="52c2f-178">A tárfiók erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="52c2f-178">The storage account resource id</span></span>

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

### <span data-ttu-id="52c2f-179">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="52c2f-179">-StorageKeyType</span></span>
<span data-ttu-id="52c2f-180">Meghatározza, hogy melyik tárelérési kulcsot kell használnia.</span><span class="sxs-lookup"><span data-stu-id="52c2f-180">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="52c2f-181">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="52c2f-181">-WorkspaceResourceId</span></span>
<span data-ttu-id="52c2f-182">Annak a Log Analytics-munkaterületnek a munkaterület-azonosítója (a Log Analytics munkaterületének erőforrás-azonosítója), amelyre naplókat szeretne küldeni.</span><span class="sxs-lookup"><span data-stu-id="52c2f-182">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Audit Logs.</span></span> <span data-ttu-id="52c2f-183">Példa: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span><span class="sxs-lookup"><span data-stu-id="52c2f-183">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

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

### <span data-ttu-id="52c2f-184">-Confirm</span><span class="sxs-lookup"><span data-stu-id="52c2f-184">-Confirm</span></span>
<span data-ttu-id="52c2f-185">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="52c2f-185">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52c2f-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52c2f-186">-WhatIf</span></span>
<span data-ttu-id="52c2f-187">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="52c2f-187">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="52c2f-188">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="52c2f-188">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52c2f-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52c2f-189">CommonParameters</span></span>
<span data-ttu-id="52c2f-190">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52c2f-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52c2f-191">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="52c2f-191">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52c2f-192">INPUTS</span><span class="sxs-lookup"><span data-stu-id="52c2f-192">INPUTS</span></span>

### <span data-ttu-id="52c2f-193">System.String</span><span class="sxs-lookup"><span data-stu-id="52c2f-193">System.String</span></span>

### <span data-ttu-id="52c2f-194">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="52c2f-194">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="52c2f-195">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span><span class="sxs-lookup"><span data-stu-id="52c2f-195">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span></span>

### <span data-ttu-id="52c2f-196">System.String[]</span><span class="sxs-lookup"><span data-stu-id="52c2f-196">System.String[]</span></span>

### <span data-ttu-id="52c2f-197">System.Guid</span><span class="sxs-lookup"><span data-stu-id="52c2f-197">System.Guid</span></span>

### <span data-ttu-id="52c2f-198">System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="52c2f-198">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="52c2f-199">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseAuditModel</span><span class="sxs-lookup"><span data-stu-id="52c2f-199">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseAuditModel</span></span>

## <span data-ttu-id="52c2f-200">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="52c2f-200">OUTPUTS</span></span>

### <span data-ttu-id="52c2f-201">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="52c2f-201">System.Boolean</span></span>

## <span data-ttu-id="52c2f-202">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="52c2f-202">NOTES</span></span>

## <span data-ttu-id="52c2f-203">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="52c2f-203">RELATED LINKS</span></span>
