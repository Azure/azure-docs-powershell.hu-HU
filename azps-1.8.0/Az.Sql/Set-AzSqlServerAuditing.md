---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAuditing.md
ms.openlocfilehash: 44db866488459382a3b66f77328b5cbc9259754b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668758"
---
# <span data-ttu-id="dca4e-101">Set-AzSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="dca4e-101">Set-AzSqlServerAuditing</span></span>

## <span data-ttu-id="dca4e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dca4e-102">SYNOPSIS</span></span>
<span data-ttu-id="dca4e-103">Az Azure SQL Server-kiszolgálók naplózási beállításainak módosítása</span><span class="sxs-lookup"><span data-stu-id="dca4e-103">Changes the auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="dca4e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dca4e-104">SYNTAX</span></span>

### <span data-ttu-id="dca4e-105">DefaultParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="dca4e-105">DefaultParameterSet (Default)</span></span>
```
Set-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob] [-BlobStorage]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dca4e-106">StorageAccountSubscriptionIdSet</span><span class="sxs-lookup"><span data-stu-id="dca4e-106">StorageAccountSubscriptionIdSet</span></span>
```
Set-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob] [-BlobStorage]
 -StorageAccountName <String> -StorageAccountSubscriptionId <Guid> [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dca4e-107">EventHubSet</span><span class="sxs-lookup"><span data-stu-id="dca4e-107">EventHubSet</span></span>
```
Set-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dca4e-108">LogAnalyticsSet</span><span class="sxs-lookup"><span data-stu-id="dca4e-108">LogAnalyticsSet</span></span>
```
Set-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob]
 [-WorkspaceResourceId <String>] [-LogAnalytics] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dca4e-109">BlobStorageByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="dca4e-109">BlobStorageByParentResourceSet</span></span>
```
Set-AzSqlServerAuditing -InputObject <AzureSqlServerModel> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob] [-BlobStorage]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dca4e-110">StorageAccountSubscriptionIdByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="dca4e-110">StorageAccountSubscriptionIdByParentResourceSet</span></span>
```
Set-AzSqlServerAuditing -InputObject <AzureSqlServerModel> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob] [-BlobStorage]
 -StorageAccountName <String> -StorageAccountSubscriptionId <Guid> [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dca4e-111">EventHubByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="dca4e-111">EventHubByParentResourceSet</span></span>
```
Set-AzSqlServerAuditing -InputObject <AzureSqlServerModel> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dca4e-112">LogAnalyticsByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="dca4e-112">LogAnalyticsByParentResourceSet</span></span>
```
Set-AzSqlServerAuditing -InputObject <AzureSqlServerModel> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob]
 [-WorkspaceResourceId <String>] [-LogAnalytics] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dca4e-113">Leírás</span><span class="sxs-lookup"><span data-stu-id="dca4e-113">DESCRIPTION</span></span>
<span data-ttu-id="dca4e-114">A **set-AzSqlServerAuditing** parancsmag az Azure SQL Server-kiszolgálók naplózási beállításait módosítja.</span><span class="sxs-lookup"><span data-stu-id="dca4e-114">The **Set-AzSqlServerAuditing** cmdlet changes the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="dca4e-115">A parancsmag használatához a *ResourceGroupName* és a *kiszolgálónév* paraméterrel keresse meg a kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="dca4e-115">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="dca4e-116">A naplók rendeltetési helyét az alábbi kapcsoló paraméterek egyikének megadásával határozhatja meg: BlobStorage, LogAnalytics vagy EventHub (ha nincs megadva, az alapértelmezett érték a BlobStorage).</span><span class="sxs-lookup"><span data-stu-id="dca4e-116">The audit logs destination is determined by specifying one of the following switch parameters: BlobStorage, LogAnalytics or EventHub (if none is specified, the default is BlobStorage).</span></span>
<span data-ttu-id="dca4e-117">A házirend engedélyezéséhez vagy letiltásához használja az *állami* paramétert.</span><span class="sxs-lookup"><span data-stu-id="dca4e-117">Use the *State* parameter to enable/disable the policy.</span></span>
<span data-ttu-id="dca4e-118">Ha a naplók a blob-tárolók, a *StorageAccountName* paraméterrel határozhatja meg a naplók tárolási fiókját és a *StorageKeyType* paramétert a tárolási kulcsok meghatározásához.</span><span class="sxs-lookup"><span data-stu-id="dca4e-118">When audit logs destination is blob storage, specify the *StorageAccountName* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="dca4e-119">A naplók adatmegőrzését úgy is megadhatja, hogy az *RetentionInDays* paraméter értékét adja meg a naplók időszakának meghatározásához.</span><span class="sxs-lookup"><span data-stu-id="dca4e-119">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>
<span data-ttu-id="dca4e-120">Ha a parancsmag sikerrel jár, és a *PassThru* paramétert használja, az a kiszolgálói azonosítók mellett a jelenlegi naplózási beállításokat leíró objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="dca4e-120">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current auditing settings in addition to the server identifiers.</span></span>
<span data-ttu-id="dca4e-121">A kiszolgálói azonosítók tartalmazzák, de nem korlátozódnak a **ResourceGroupName** és a **kiszolgáló_neve** -ra.</span><span class="sxs-lookup"><span data-stu-id="dca4e-121">Server identifiers include, but are not limited to, **ResourceGroupName** and **ServerName**.</span></span>

## <span data-ttu-id="dca4e-122">Példák</span><span class="sxs-lookup"><span data-stu-id="dca4e-122">EXAMPLES</span></span>

### <span data-ttu-id="dca4e-123">1. példa: az Azure SQL Server blob-tároló naplózási házirendjének engedélyezése</span><span class="sxs-lookup"><span data-stu-id="dca4e-123">Example 1: Enable the blob storage auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22"
```

### <span data-ttu-id="dca4e-124">2. példa: az Azure SQL Server blob-tároló naplózási házirendjének letiltása</span><span class="sxs-lookup"><span data-stu-id="dca4e-124">Example 2: Disable the blob storage auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

### <span data-ttu-id="dca4e-125">3. példa: az Azure SQL Server blob-tároló naplózási házirendjének engedélyezése másik előfizetésből származó tárolási fiók használatával</span><span class="sxs-lookup"><span data-stu-id="dca4e-125">Example 3: Enable the blob storage auditing policy of an Azure SQL server using a storage account from a different subscription</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -StorageAccountSubscriptionId "7fe3301d-31d3-4668-af5e-211a890ba6e3"
```

### <span data-ttu-id="dca4e-126">Példa 4: a blob-tároló naplózási házirendjének engedélyezése az Azure SQL Server speciális szűrési szolgáltatásával a T-SQL predikátummal</span><span class="sxs-lookup"><span data-stu-id="dca4e-126">Example 4: Enable the blob storage auditing policy of an Azure SQL server with advanced filtering using a T-SQL predicate</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -PredicateExpression "statement <> 'select 1'"
```

### <span data-ttu-id="dca4e-127">Példa 5: az Azure SQL Server rendszer blob-naplózási házirendjének speciális szűrési beállításának eltávolítása</span><span class="sxs-lookup"><span data-stu-id="dca4e-127">Example 5: Remove the advanced filtering setting from the blob auditing storage policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -PredicateExpression ""
```

### <span data-ttu-id="dca4e-128">Példa 6: az Azure SQL Server esemény központi naplózási házirendjének engedélyezése</span><span class="sxs-lookup"><span data-stu-id="dca4e-128">Example 6: Enable the event hub auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId"
```

### <span data-ttu-id="dca4e-129">7. példa: az Azure SQL Server esemény központi naplózási házirendjének letiltása</span><span class="sxs-lookup"><span data-stu-id="dca4e-129">Example 7: Disable the event hub auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubName
```

### <span data-ttu-id="dca4e-130">8. példa: az Azure SQL Server log Analytics naplózási házirendjének engedélyezése</span><span class="sxs-lookup"><span data-stu-id="dca4e-130">Example 8: Enable the log analytics auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalytics -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="dca4e-131">Példa 9: az Azure SQL Server log Analytics naplózási házirendjének letiltása</span><span class="sxs-lookup"><span data-stu-id="dca4e-131">Example 9: Disable the log analytics auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalytics
```

### <span data-ttu-id="dca4e-132">10. példa: az Azure SQL Server rendszerhez tartozó log Analytics naplózási házirendjének letiltása a csővezetéken keresztül</span><span class="sxs-lookup"><span data-stu-id="dca4e-132">Example 10: Disable, through pipeline, the log analytics auditing policy of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Set-AzSqlServerAuditing -LogAnalytics -State Disabled
```

## <span data-ttu-id="dca4e-133">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dca4e-133">PARAMETERS</span></span>

### <span data-ttu-id="dca4e-134">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dca4e-134">-AsJob</span></span>
<span data-ttu-id="dca4e-135">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="dca4e-135">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dca4e-136">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="dca4e-136">-AuditActionGroup</span></span>
<span data-ttu-id="dca4e-137">A használni kívánt műveleti csoportok a következő kombinációk: Ez a művelet naplózza az adatbázissal végzett összes lekérdezést és tárolt eljárást, valamint a sikeres és sikertelen bejelentkezéseket:</span><span class="sxs-lookup"><span data-stu-id="dca4e-137">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="dca4e-138">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="dca4e-138">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="dca4e-139">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="dca4e-139">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="dca4e-140">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="dca4e-140">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  
<span data-ttu-id="dca4e-141">Ez a fenti kombináció egyben az alapértelmezés szerint konfigurált halmaz.</span><span class="sxs-lookup"><span data-stu-id="dca4e-141">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="dca4e-142">Ezek a csoportok az adatbázissal szemben végrehajtott összes SQL-utasítást és tárolt eljárást lefoglalják, és nem használhatók együtt más csoportokkal, mert ez a művelet duplikálja a naplókat.</span><span class="sxs-lookup"><span data-stu-id="dca4e-142">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="dca4e-143">További információ: https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="dca4e-143">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="dca4e-144">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="dca4e-144">-BlobStorage</span></span>
<span data-ttu-id="dca4e-145">Megadja, hogy a naplók a blob-tárolók legyenek</span><span class="sxs-lookup"><span data-stu-id="dca4e-145">Specifies that audit logs destination is blob storage</span></span>

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

### <span data-ttu-id="dca4e-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dca4e-146">-DefaultProfile</span></span>
<span data-ttu-id="dca4e-147">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dca4e-147">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dca4e-148">-EventHub</span><span class="sxs-lookup"><span data-stu-id="dca4e-148">-EventHub</span></span>
<span data-ttu-id="dca4e-149">Azt adja meg, hogy a naplók cél az esemény középpontja</span><span class="sxs-lookup"><span data-stu-id="dca4e-149">Specifies that audit logs destination is event hub</span></span>

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

### <span data-ttu-id="dca4e-150">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="dca4e-150">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="dca4e-151">Az esemény-hub engedélyezési szabályának erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="dca4e-151">The resource Id for the event hub authorization rule</span></span>

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

### <span data-ttu-id="dca4e-152">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="dca4e-152">-EventHubName</span></span>
<span data-ttu-id="dca4e-153">Az esemény központja neve.</span><span class="sxs-lookup"><span data-stu-id="dca4e-153">The name of the event hub.</span></span> <span data-ttu-id="dca4e-154">Ha a EventHubAuthorizationRuleResourceId megadásakor nincs megadva, az alapértelmezett esemény hub lesz kiválasztva.</span><span class="sxs-lookup"><span data-stu-id="dca4e-154">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

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

### <span data-ttu-id="dca4e-155">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dca4e-155">-InputObject</span></span>
<span data-ttu-id="dca4e-156">A kiszolgálói objektum a naplózási házirend kezeléséhez.</span><span class="sxs-lookup"><span data-stu-id="dca4e-156">The server object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: BlobStorageByParentResourceSet, StorageAccountSubscriptionIdByParentResourceSet, EventHubByParentResourceSet, LogAnalyticsByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dca4e-157">-LogAnalytics</span><span class="sxs-lookup"><span data-stu-id="dca4e-157">-LogAnalytics</span></span>
<span data-ttu-id="dca4e-158">Azt adja meg, hogy a naplók a naplózási naplókat jelentik</span><span class="sxs-lookup"><span data-stu-id="dca4e-158">Specifies that audit logs destination is log analytics</span></span>

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

### <span data-ttu-id="dca4e-159">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dca4e-159">-PassThru</span></span>
<span data-ttu-id="dca4e-160">Azt adja meg, hogy a naplózási házirendet a parancsmag-végrehajtás végén szeretné-e kivenni.</span><span class="sxs-lookup"><span data-stu-id="dca4e-160">Specifies whether to output the auditing policy at end of cmdlet execution</span></span>

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

### <span data-ttu-id="dca4e-161">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="dca4e-161">-PredicateExpression</span></span>
<span data-ttu-id="dca4e-162">A naplók szűréséhez használt T-SQL predikátum (WHERE záradék).</span><span class="sxs-lookup"><span data-stu-id="dca4e-162">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="dca4e-163">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dca4e-163">-ResourceGroupName</span></span>
<span data-ttu-id="dca4e-164">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="dca4e-164">The name of the resource group.</span></span>

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

### <span data-ttu-id="dca4e-165">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="dca4e-165">-RetentionInDays</span></span>
<span data-ttu-id="dca4e-166">A naplók retenciós napjainak száma.</span><span class="sxs-lookup"><span data-stu-id="dca4e-166">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="dca4e-167">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="dca4e-167">-ServerName</span></span>
<span data-ttu-id="dca4e-168">SQL-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="dca4e-168">SQL server name.</span></span>

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

### <span data-ttu-id="dca4e-169">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="dca4e-169">-State</span></span>
<span data-ttu-id="dca4e-170">A házirend állapota.</span><span class="sxs-lookup"><span data-stu-id="dca4e-170">The state of the policy.</span></span>

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

### <span data-ttu-id="dca4e-171">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="dca4e-171">-StorageAccountName</span></span>
<span data-ttu-id="dca4e-172">A tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="dca4e-172">The name of the storage account.</span></span>

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

### <span data-ttu-id="dca4e-173">-StorageAccountSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dca4e-173">-StorageAccountSubscriptionId</span></span>
<span data-ttu-id="dca4e-174">A Storage Account előfizetés azonosítója</span><span class="sxs-lookup"><span data-stu-id="dca4e-174">The storage account subscription id</span></span>

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

### <span data-ttu-id="dca4e-175">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="dca4e-175">-StorageKeyType</span></span>
<span data-ttu-id="dca4e-176">Itt adhatja meg, hogy a tárterület-hozzáférési kulcsok közül melyik használható.</span><span class="sxs-lookup"><span data-stu-id="dca4e-176">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="dca4e-177">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="dca4e-177">-WorkspaceResourceId</span></span>
<span data-ttu-id="dca4e-178">A napló Analytics-munkaterületének erőforrás-azonosítója (log Analytics-munkaterületen), amelybe naplókat szeretne küldeni.</span><span class="sxs-lookup"><span data-stu-id="dca4e-178">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Audit Logs.</span></span> <span data-ttu-id="dca4e-179">Példa:/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span><span class="sxs-lookup"><span data-stu-id="dca4e-179">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

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

### <span data-ttu-id="dca4e-180">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="dca4e-180">-Confirm</span></span>
<span data-ttu-id="dca4e-181">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="dca4e-181">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dca4e-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dca4e-182">-WhatIf</span></span>
<span data-ttu-id="dca4e-183">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="dca4e-183">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dca4e-184">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dca4e-184">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dca4e-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dca4e-185">CommonParameters</span></span>
<span data-ttu-id="dca4e-186">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dca4e-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dca4e-187">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="dca4e-187">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dca4e-188">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dca4e-188">INPUTS</span></span>

### <span data-ttu-id="dca4e-189">System. String</span><span class="sxs-lookup"><span data-stu-id="dca4e-189">System.String</span></span>

### <span data-ttu-id="dca4e-190">Microsoft. Azure. Command. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="dca4e-190">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="dca4e-191">Microsoft. Azure. Command. SQL. könyvvizsgálat. Model. AuditActionGroups []</span><span class="sxs-lookup"><span data-stu-id="dca4e-191">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span></span>

### <span data-ttu-id="dca4e-192">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="dca4e-192">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="dca4e-193">System. GUID</span><span class="sxs-lookup"><span data-stu-id="dca4e-193">System.Guid</span></span>

### <span data-ttu-id="dca4e-194">System. null ' 1 [[System. UInt32, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="dca4e-194">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="dca4e-195">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dca4e-195">OUTPUTS</span></span>

### <span data-ttu-id="dca4e-196">Microsoft. Azure. Command. SQL. könyvvizsgálat. Model. ServerBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="dca4e-196">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="dca4e-197">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dca4e-197">NOTES</span></span>

## <span data-ttu-id="dca4e-198">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dca4e-198">RELATED LINKS</span></span>
