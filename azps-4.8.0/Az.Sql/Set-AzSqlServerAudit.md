---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Set-AzSqlServerAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAudit.md
ms.openlocfilehash: ec88d8ff9f5a514a3b1b5dcd9ecb917ee348b900
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183861"
---
# <span data-ttu-id="42cbd-101">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="42cbd-101">Set-AzSqlServerAudit</span></span>

## <span data-ttu-id="42cbd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="42cbd-102">SYNOPSIS</span></span>
<span data-ttu-id="42cbd-103">Az Azure SQL Server-kiszolgálók naplózási beállításainak módosítása</span><span class="sxs-lookup"><span data-stu-id="42cbd-103">Changes the auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="42cbd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="42cbd-104">SYNTAX</span></span>

### <span data-ttu-id="42cbd-105">ServerParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="42cbd-105">ServerParameterSet (Default)</span></span>
```
Set-AzSqlServerAudit [-AuditActionGroup <AuditActionGroups[]>] [-PredicateExpression <String>]
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-EventHubTargetState <String>] [-EventHubName <String>]
 [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42cbd-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="42cbd-106">ServerObjectParameterSet</span></span>
```
Set-AzSqlServerAudit [-AuditActionGroup <AuditActionGroups[]>] [-PredicateExpression <String>]
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-EventHubTargetState <String>] [-EventHubName <String>]
 [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] -ServerObject <AzureSqlServerModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42cbd-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="42cbd-107">DESCRIPTION</span></span>
<span data-ttu-id="42cbd-108">A **set-AzSqlServerAudit** parancsmag az Azure SQL Server-kiszolgálók naplózási beállításait módosítja.</span><span class="sxs-lookup"><span data-stu-id="42cbd-108">The **Set-AzSqlServerAudit** cmdlet changes the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="42cbd-109">A parancsmag használatához a *ResourceGroupName* és a *kiszolgálónév* paraméterrel keresse meg a kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="42cbd-109">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="42cbd-110">Ha a blob-tároló a naplók rendeltetése, akkor a *StorageAccountResourceId* paraméterrel határozhatja meg a naplók tárolási fiókját és a *StorageKeyType* paramétert a tárolási kulcsok meghatározásához.</span><span class="sxs-lookup"><span data-stu-id="42cbd-110">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="42cbd-111">A naplók adatmegőrzését úgy is megadhatja, hogy az *RetentionInDays* paraméter értékét adja meg a naplók időszakának meghatározásához.</span><span class="sxs-lookup"><span data-stu-id="42cbd-111">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

## <span data-ttu-id="42cbd-112">Példák</span><span class="sxs-lookup"><span data-stu-id="42cbd-112">EXAMPLES</span></span>

### <span data-ttu-id="42cbd-113">1. példa: az Azure SQL Server blob-tároló naplózási házirendjének engedélyezése</span><span class="sxs-lookup"><span data-stu-id="42cbd-113">Example 1: Enable the blob storage auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### <span data-ttu-id="42cbd-114">2. példa: az Azure SQL Server blob-tároló naplózási házirendjének letiltása</span><span class="sxs-lookup"><span data-stu-id="42cbd-114">Example 2: Disable the blob storage auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="42cbd-115">3. példa: a blob-tároló naplózási házirendjének engedélyezése az Azure SQL Server speciális szűrési házirendjének használatával a T-SQL predikátummal</span><span class="sxs-lookup"><span data-stu-id="42cbd-115">Example 3: Enable the blob storage auditing policy of an Azure SQL server with advanced filtering using a T-SQL predicate</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -PredicateExpression "statement <> 'select 1'"
```

### <span data-ttu-id="42cbd-116">4. példa: az Advanced szűrési beállítás eltávolítása egy Azure SQL Server naplózási házirendjéből</span><span class="sxs-lookup"><span data-stu-id="42cbd-116">Example 4: Remove the advanced filtering setting from the auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -PredicateExpression ""
```

### <span data-ttu-id="42cbd-117">Példa 5: az Azure SQL Server esemény központi naplózási házirendjének engedélyezése</span><span class="sxs-lookup"><span data-stu-id="42cbd-117">Example 5: Enable the event hub auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId"
```

### <span data-ttu-id="42cbd-118">Példa 6: az Azure SQL Server esemény központi naplózási házirendjének letiltása</span><span class="sxs-lookup"><span data-stu-id="42cbd-118">Example 6: Disable the event hub auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubTargetState Disabled
```

### <span data-ttu-id="42cbd-119">7. példa: az Azure SQL Server log Analytics naplózási házirendjének engedélyezése</span><span class="sxs-lookup"><span data-stu-id="42cbd-119">Example 7: Enable the log analytics auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="42cbd-120">8. példa: a log Analytics naplózási házirendjének letiltása egy Azure SQL Server-kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="42cbd-120">Example 8: Disable the log analytics auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="42cbd-121">Példa 9: az Azure SQL Server naplózási házirendjének letiltása a csővezetéken keresztül</span><span class="sxs-lookup"><span data-stu-id="42cbd-121">Example 9: Disable, through pipeline, the log analytics auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Set-AzSqlServerAudit -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="42cbd-122">10. példa: az Azure SQL Server-alapú naplózási rekordok küldésének letiltása blob-tárterületre, és a naplózás engedélyezése a naplózási elemzéshez.</span><span class="sxs-lookup"><span data-stu-id="42cbd-122">Example 10: Disable sending audit records of an Azure SQL server to blob storage, and enable sending them to log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="42cbd-123">11-es példa: az Azure SQL Server-alapú naplózási rekordok küldésének engedélyezése a blob-tároló, az esemény-hub és a log Analytics számára.</span><span class="sxs-lookup"><span data-stu-id="42cbd-123">Example 11: Enable sending audit records of an Azure SQL server to blob storage, event hub and log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId" -LogAnalyticsTargetState Enabled  -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

## <span data-ttu-id="42cbd-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="42cbd-124">PARAMETERS</span></span>

### <span data-ttu-id="42cbd-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="42cbd-125">-AsJob</span></span>
<span data-ttu-id="42cbd-126">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="42cbd-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="42cbd-127">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="42cbd-127">-AuditActionGroup</span></span>
<span data-ttu-id="42cbd-128">A használni kívánt műveleti csoportok a következő kombinációk: Ez a művelet naplózza az adatbázissal végzett összes lekérdezést és tárolt eljárást, valamint a sikeres és sikertelen bejelentkezéseket:</span><span class="sxs-lookup"><span data-stu-id="42cbd-128">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="42cbd-129">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="42cbd-129">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="42cbd-130">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="42cbd-130">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="42cbd-131">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="42cbd-131">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  
<span data-ttu-id="42cbd-132">Ez a fenti kombináció egyben az alapértelmezés szerint konfigurált halmaz.</span><span class="sxs-lookup"><span data-stu-id="42cbd-132">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="42cbd-133">Ezek a csoportok az adatbázissal szemben végrehajtott összes SQL-utasítást és tárolt eljárást lefoglalják, és nem használhatók együtt más csoportokkal, mert ez a művelet duplikálja a naplókat.</span><span class="sxs-lookup"><span data-stu-id="42cbd-133">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="42cbd-134">További információ: https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="42cbd-134">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="42cbd-135">-BlobStorageTargetState</span><span class="sxs-lookup"><span data-stu-id="42cbd-135">-BlobStorageTargetState</span></span>
<span data-ttu-id="42cbd-136">Azt jelzi, hogy a blob-tároló a rekordok naplózására szolgáló cél-e.</span><span class="sxs-lookup"><span data-stu-id="42cbd-136">Indicates whether blob storage is a destination for audit records.</span></span>

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

### <span data-ttu-id="42cbd-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42cbd-137">-DefaultProfile</span></span>
<span data-ttu-id="42cbd-138">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="42cbd-138">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42cbd-139">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="42cbd-139">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="42cbd-140">Az esemény-hub engedélyezési szabályának erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="42cbd-140">The resource Id for the event hub authorization rule</span></span>

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

### <span data-ttu-id="42cbd-141">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="42cbd-141">-EventHubName</span></span>
<span data-ttu-id="42cbd-142">Az esemény központja neve.</span><span class="sxs-lookup"><span data-stu-id="42cbd-142">The name of the event hub.</span></span> <span data-ttu-id="42cbd-143">Ha a EventHubAuthorizationRuleResourceId megadásakor nincs megadva, az alapértelmezett esemény hub lesz kiválasztva.</span><span class="sxs-lookup"><span data-stu-id="42cbd-143">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

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

### <span data-ttu-id="42cbd-144">-EventHubTargetState</span><span class="sxs-lookup"><span data-stu-id="42cbd-144">-EventHubTargetState</span></span>
<span data-ttu-id="42cbd-145">Azt jelzi, hogy az esemény központja a rekordok naplózásának a rendeltetése.</span><span class="sxs-lookup"><span data-stu-id="42cbd-145">Indicates whether event hub is a destination for audit records.</span></span>

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

### <span data-ttu-id="42cbd-146">-LogAnalyticsTargetState</span><span class="sxs-lookup"><span data-stu-id="42cbd-146">-LogAnalyticsTargetState</span></span>
<span data-ttu-id="42cbd-147">Azt jelzi, hogy a napló-elemzés a rekordok naplózási célja-e.</span><span class="sxs-lookup"><span data-stu-id="42cbd-147">Indicates whether log analytics is a destination for audit records.</span></span>

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

### <span data-ttu-id="42cbd-148">-PassThru</span><span class="sxs-lookup"><span data-stu-id="42cbd-148">-PassThru</span></span>
<span data-ttu-id="42cbd-149">Azt adja meg, hogy a naplózási házirendet a parancsmag-végrehajtás végén szeretné-e kivenni.</span><span class="sxs-lookup"><span data-stu-id="42cbd-149">Specifies whether to output the auditing policy at end of cmdlet execution</span></span>

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

### <span data-ttu-id="42cbd-150">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="42cbd-150">-PredicateExpression</span></span>
<span data-ttu-id="42cbd-151">A naplók szűréséhez használt T-SQL predikátum (WHERE záradék).</span><span class="sxs-lookup"><span data-stu-id="42cbd-151">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="42cbd-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42cbd-152">-ResourceGroupName</span></span>
<span data-ttu-id="42cbd-153">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="42cbd-153">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42cbd-154">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="42cbd-154">-RetentionInDays</span></span>
<span data-ttu-id="42cbd-155">A naplók retenciós napjainak száma.</span><span class="sxs-lookup"><span data-stu-id="42cbd-155">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="42cbd-156">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="42cbd-156">-ServerName</span></span>
<span data-ttu-id="42cbd-157">SQL-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="42cbd-157">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42cbd-158">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="42cbd-158">-ServerObject</span></span>
<span data-ttu-id="42cbd-159">A kiszolgálói objektum a naplózási házirend kezeléséhez.</span><span class="sxs-lookup"><span data-stu-id="42cbd-159">The server object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: ServerObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="42cbd-160">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="42cbd-160">-StorageAccountResourceId</span></span>
<span data-ttu-id="42cbd-161">A tárolási fiók erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="42cbd-161">The storage account resource id</span></span>

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

### <span data-ttu-id="42cbd-162">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="42cbd-162">-StorageKeyType</span></span>
<span data-ttu-id="42cbd-163">Itt adhatja meg, hogy a tárterület-hozzáférési kulcsok közül melyik használható.</span><span class="sxs-lookup"><span data-stu-id="42cbd-163">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="42cbd-164">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="42cbd-164">-WorkspaceResourceId</span></span>
<span data-ttu-id="42cbd-165">A napló Analytics-munkaterületének erőforrás-azonosítója (log Analytics-munkaterületen), amelybe naplókat szeretne küldeni.</span><span class="sxs-lookup"><span data-stu-id="42cbd-165">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Audit Logs.</span></span> <span data-ttu-id="42cbd-166">Példa:/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span><span class="sxs-lookup"><span data-stu-id="42cbd-166">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

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

### <span data-ttu-id="42cbd-167">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="42cbd-167">-Confirm</span></span>
<span data-ttu-id="42cbd-168">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="42cbd-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42cbd-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42cbd-169">-WhatIf</span></span>
<span data-ttu-id="42cbd-170">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="42cbd-170">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="42cbd-171">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="42cbd-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42cbd-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42cbd-172">CommonParameters</span></span>
<span data-ttu-id="42cbd-173">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="42cbd-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42cbd-174">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="42cbd-174">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42cbd-175">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="42cbd-175">INPUTS</span></span>

### <span data-ttu-id="42cbd-176">System. String</span><span class="sxs-lookup"><span data-stu-id="42cbd-176">System.String</span></span>

### <span data-ttu-id="42cbd-177">Microsoft. Azure. Command. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="42cbd-177">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="42cbd-178">Microsoft. Azure. Command. SQL. könyvvizsgálat. Model. AuditActionGroups []</span><span class="sxs-lookup"><span data-stu-id="42cbd-178">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span></span>

### <span data-ttu-id="42cbd-179">System. GUID</span><span class="sxs-lookup"><span data-stu-id="42cbd-179">System.Guid</span></span>

### <span data-ttu-id="42cbd-180">System. null ' 1 [[System. UInt32, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="42cbd-180">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="42cbd-181">Microsoft. Azure. Command. SQL. könyvvizsgálat. Model. ServerAuditModel</span><span class="sxs-lookup"><span data-stu-id="42cbd-181">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerAuditModel</span></span>

## <span data-ttu-id="42cbd-182">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="42cbd-182">OUTPUTS</span></span>

### <span data-ttu-id="42cbd-183">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="42cbd-183">System.Boolean</span></span>

## <span data-ttu-id="42cbd-184">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="42cbd-184">NOTES</span></span>

## <span data-ttu-id="42cbd-185">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="42cbd-185">RELATED LINKS</span></span>
