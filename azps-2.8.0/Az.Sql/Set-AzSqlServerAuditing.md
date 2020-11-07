---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAuditing.md
ms.openlocfilehash: e9d3e7ca009a756526bc0cb150ebdb6c124df032
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839328"
---
# <span data-ttu-id="ba9f1-101">Set-AzSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="ba9f1-101">Set-AzSqlServerAuditing</span></span>

## <span data-ttu-id="ba9f1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ba9f1-102">SYNOPSIS</span></span>
<span data-ttu-id="ba9f1-103">**Fontos: Ez a parancsmag elavult, a [set-AzSqlServerAudit](https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserveraudit) a helyére lép.**</span><span class="sxs-lookup"><span data-stu-id="ba9f1-103">**Important: This cmdlet is deprecated, [Set-AzSqlServerAudit](https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserveraudit) is replacing it.**</span></span>

<span data-ttu-id="ba9f1-104">Az Azure SQL Server-kiszolgálók naplózási beállításainak módosítása</span><span class="sxs-lookup"><span data-stu-id="ba9f1-104">Changes the auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="ba9f1-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ba9f1-105">SYNTAX</span></span>

### <span data-ttu-id="ba9f1-106">DefaultParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ba9f1-106">DefaultParameterSet (Default)</span></span>
```
Set-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob] [-BlobStorage]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba9f1-107">StorageAccountSubscriptionIdSet</span><span class="sxs-lookup"><span data-stu-id="ba9f1-107">StorageAccountSubscriptionIdSet</span></span>
```
Set-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob] [-BlobStorage]
 -StorageAccountName <String> -StorageAccountSubscriptionId <Guid> [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ba9f1-108">EventHubSet</span><span class="sxs-lookup"><span data-stu-id="ba9f1-108">EventHubSet</span></span>
```
Set-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba9f1-109">LogAnalyticsSet</span><span class="sxs-lookup"><span data-stu-id="ba9f1-109">LogAnalyticsSet</span></span>
```
Set-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob]
 [-WorkspaceResourceId <String>] [-LogAnalytics] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba9f1-110">BlobStorageByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="ba9f1-110">BlobStorageByParentResourceSet</span></span>
```
Set-AzSqlServerAuditing -InputObject <AzureSqlServerModel> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob] [-BlobStorage]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba9f1-111">StorageAccountSubscriptionIdByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="ba9f1-111">StorageAccountSubscriptionIdByParentResourceSet</span></span>
```
Set-AzSqlServerAuditing -InputObject <AzureSqlServerModel> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob] [-BlobStorage]
 -StorageAccountName <String> -StorageAccountSubscriptionId <Guid> [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ba9f1-112">EventHubByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="ba9f1-112">EventHubByParentResourceSet</span></span>
```
Set-AzSqlServerAuditing -InputObject <AzureSqlServerModel> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba9f1-113">LogAnalyticsByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="ba9f1-113">LogAnalyticsByParentResourceSet</span></span>
```
Set-AzSqlServerAuditing -InputObject <AzureSqlServerModel> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob]
 [-WorkspaceResourceId <String>] [-LogAnalytics] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba9f1-114">Leírás</span><span class="sxs-lookup"><span data-stu-id="ba9f1-114">DESCRIPTION</span></span>
<span data-ttu-id="ba9f1-115">A **set-AzSqlServerAuditing** parancsmag az Azure SQL Server-kiszolgálók naplózási beállításait módosítja.</span><span class="sxs-lookup"><span data-stu-id="ba9f1-115">The **Set-AzSqlServerAuditing** cmdlet changes the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="ba9f1-116">A parancsmag használatához a *ResourceGroupName* és a *kiszolgálónév* paraméterrel keresse meg a kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="ba9f1-116">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="ba9f1-117">A naplók rendeltetési helyét az alábbi kapcsoló paraméterek egyikének megadásával határozhatja meg: BlobStorage, LogAnalytics vagy EventHub (ha nincs megadva, az alapértelmezett érték a BlobStorage).</span><span class="sxs-lookup"><span data-stu-id="ba9f1-117">The audit logs destination is determined by specifying one of the following switch parameters: BlobStorage, LogAnalytics or EventHub (if none is specified, the default is BlobStorage).</span></span>
<span data-ttu-id="ba9f1-118">A házirend engedélyezéséhez vagy letiltásához használja az *állami* paramétert.</span><span class="sxs-lookup"><span data-stu-id="ba9f1-118">Use the *State* parameter to enable/disable the policy.</span></span>
<span data-ttu-id="ba9f1-119">Ha a naplók a blob-tárolók, a *StorageAccountName* paraméterrel határozhatja meg a naplók tárolási fiókját és a *StorageKeyType* paramétert a tárolási kulcsok meghatározásához.</span><span class="sxs-lookup"><span data-stu-id="ba9f1-119">When audit logs destination is blob storage, specify the *StorageAccountName* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="ba9f1-120">A naplók adatmegőrzését úgy is megadhatja, hogy az *RetentionInDays* paraméter értékét adja meg a naplók időszakának meghatározásához.</span><span class="sxs-lookup"><span data-stu-id="ba9f1-120">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>
<span data-ttu-id="ba9f1-121">Ha a parancsmag sikerrel jár, és a *PassThru* paramétert használja, az a kiszolgálói azonosítók mellett a jelenlegi naplózási beállításokat leíró objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="ba9f1-121">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current auditing settings in addition to the server identifiers.</span></span>
<span data-ttu-id="ba9f1-122">A kiszolgálói azonosítók tartalmazzák, de nem korlátozódnak a **ResourceGroupName** és a **kiszolgáló_neve** -ra.</span><span class="sxs-lookup"><span data-stu-id="ba9f1-122">Server identifiers include, but are not limited to, **ResourceGroupName** and **ServerName**.</span></span>

## <span data-ttu-id="ba9f1-123">Példák</span><span class="sxs-lookup"><span data-stu-id="ba9f1-123">EXAMPLES</span></span>

### <span data-ttu-id="ba9f1-124">1. példa: az Azure SQL Server blob-tároló naplózási házirendjének engedélyezése</span><span class="sxs-lookup"><span data-stu-id="ba9f1-124">Example 1: Enable the blob storage auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22"
```

### <span data-ttu-id="ba9f1-125">2. példa: az Azure SQL Server blob-tároló naplózási házirendjének letiltása</span><span class="sxs-lookup"><span data-stu-id="ba9f1-125">Example 2: Disable the blob storage auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

### <span data-ttu-id="ba9f1-126">3. példa: az Azure SQL Server blob-tároló naplózási házirendjének engedélyezése másik előfizetésből származó tárolási fiók használatával</span><span class="sxs-lookup"><span data-stu-id="ba9f1-126">Example 3: Enable the blob storage auditing policy of an Azure SQL server using a storage account from a different subscription</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -StorageAccountSubscriptionId "7fe3301d-31d3-4668-af5e-211a890ba6e3"
```

### <span data-ttu-id="ba9f1-127">Példa 4: a blob-tároló naplózási házirendjének engedélyezése az Azure SQL Server speciális szűrési szolgáltatásával a T-SQL predikátummal</span><span class="sxs-lookup"><span data-stu-id="ba9f1-127">Example 4: Enable the blob storage auditing policy of an Azure SQL server with advanced filtering using a T-SQL predicate</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -PredicateExpression "statement <> 'select 1'"
```

### <span data-ttu-id="ba9f1-128">Példa 5: az Azure SQL Server rendszer blob-naplózási házirendjének speciális szűrési beállításának eltávolítása</span><span class="sxs-lookup"><span data-stu-id="ba9f1-128">Example 5: Remove the advanced filtering setting from the blob auditing storage policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -PredicateExpression ""
```

### <span data-ttu-id="ba9f1-129">Példa 6: az Azure SQL Server esemény központi naplózási házirendjének engedélyezése</span><span class="sxs-lookup"><span data-stu-id="ba9f1-129">Example 6: Enable the event hub auditing policy of an Azure SQL server</span></span>
```
$EventHubAuthorizationRule = Get-AzEventHubAuthorizationRule `
    -ResourceGroupName "ResourceGroup01" `
    -Namespace "EventHubName" `
    -Name "SharedAccessPoliceName" 

Set-AzSqlServerAuditing `
    -State Enabled `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -EventHub `
    -EventHubName "EventHubName" `
    -EventHubAuthorizationRuleResourceId $EventHubAuthorizationRule.Id
```

### <span data-ttu-id="ba9f1-130">7. példa: az Azure SQL Server esemény központi naplózási házirendjének letiltása</span><span class="sxs-lookup"><span data-stu-id="ba9f1-130">Example 7: Disable the event hub auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubName
```

### <span data-ttu-id="ba9f1-131">8. példa: az Azure SQL Server log Analytics naplózási házirendjének engedélyezése</span><span class="sxs-lookup"><span data-stu-id="ba9f1-131">Example 8: Enable the log analytics auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalytics -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="ba9f1-132">Példa 9: az Azure SQL Server log Analytics naplózási házirendjének letiltása</span><span class="sxs-lookup"><span data-stu-id="ba9f1-132">Example 9: Disable the log analytics auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalytics
```

### <span data-ttu-id="ba9f1-133">10. példa: az Azure SQL Server rendszerhez tartozó log Analytics naplózási házirendjének letiltása a csővezetéken keresztül</span><span class="sxs-lookup"><span data-stu-id="ba9f1-133">Example 10: Disable, through pipeline, the log analytics auditing policy of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Set-AzSqlServerAuditing -LogAnalytics -State Disabled
```

## <span data-ttu-id="ba9f1-134">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ba9f1-134">PARAMETERS</span></span>

### <span data-ttu-id="ba9f1-135">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ba9f1-135">-AsJob</span></span>
<span data-ttu-id="ba9f1-136">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="ba9f1-136">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ba9f1-137">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="ba9f1-137">-AuditActionGroup</span></span>
<span data-ttu-id="ba9f1-138">A használni kívánt műveleti csoportok a következő kombinációk: Ez a művelet naplózza az adatbázissal végzett összes lekérdezést és tárolt eljárást, valamint a sikeres és sikertelen bejelentkezéseket:</span><span class="sxs-lookup"><span data-stu-id="ba9f1-138">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="ba9f1-139">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="ba9f1-139">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="ba9f1-140">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="ba9f1-140">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="ba9f1-141">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="ba9f1-141">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  
<span data-ttu-id="ba9f1-142">Ez a fenti kombináció egyben az alapértelmezés szerint konfigurált halmaz.</span><span class="sxs-lookup"><span data-stu-id="ba9f1-142">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="ba9f1-143">Ezek a csoportok az adatbázissal szemben végrehajtott összes SQL-utasítást és tárolt eljárást lefoglalják, és nem használhatók együtt más csoportokkal, mert ez a művelet duplikálja a naplókat.</span><span class="sxs-lookup"><span data-stu-id="ba9f1-143">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="ba9f1-144">További információ: https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="ba9f1-144">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="ba9f1-145">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="ba9f1-145">-BlobStorage</span></span>
<span data-ttu-id="ba9f1-146">Megadja, hogy a naplók a blob-tárolók legyenek</span><span class="sxs-lookup"><span data-stu-id="ba9f1-146">Specifies that audit logs destination is blob storage</span></span>

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

### <span data-ttu-id="ba9f1-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba9f1-147">-DefaultProfile</span></span>
<span data-ttu-id="ba9f1-148">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ba9f1-148">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba9f1-149">-EventHub</span><span class="sxs-lookup"><span data-stu-id="ba9f1-149">-EventHub</span></span>
<span data-ttu-id="ba9f1-150">Azt adja meg, hogy a naplók cél az esemény középpontja</span><span class="sxs-lookup"><span data-stu-id="ba9f1-150">Specifies that audit logs destination is event hub</span></span>

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

### <span data-ttu-id="ba9f1-151">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="ba9f1-151">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="ba9f1-152">Az esemény-hub engedélyezési szabályának erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="ba9f1-152">The resource Id for the event hub authorization rule</span></span>

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

### <span data-ttu-id="ba9f1-153">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="ba9f1-153">-EventHubName</span></span>
<span data-ttu-id="ba9f1-154">Az esemény központja neve.</span><span class="sxs-lookup"><span data-stu-id="ba9f1-154">The name of the event hub.</span></span> <span data-ttu-id="ba9f1-155">Ha a EventHubAuthorizationRuleResourceId megadásakor nincs megadva, az alapértelmezett esemény hub lesz kiválasztva.</span><span class="sxs-lookup"><span data-stu-id="ba9f1-155">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

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

### <span data-ttu-id="ba9f1-156">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ba9f1-156">-InputObject</span></span>
<span data-ttu-id="ba9f1-157">A kiszolgálói objektum a naplózási házirend kezeléséhez.</span><span class="sxs-lookup"><span data-stu-id="ba9f1-157">The server object to manage its audit policy.</span></span>

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

### <span data-ttu-id="ba9f1-158">-LogAnalytics</span><span class="sxs-lookup"><span data-stu-id="ba9f1-158">-LogAnalytics</span></span>
<span data-ttu-id="ba9f1-159">Azt adja meg, hogy a naplók a naplózási naplókat jelentik</span><span class="sxs-lookup"><span data-stu-id="ba9f1-159">Specifies that audit logs destination is log analytics</span></span>

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

### <span data-ttu-id="ba9f1-160">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ba9f1-160">-PassThru</span></span>
<span data-ttu-id="ba9f1-161">Azt adja meg, hogy a naplózási házirendet a parancsmag-végrehajtás végén szeretné-e kivenni.</span><span class="sxs-lookup"><span data-stu-id="ba9f1-161">Specifies whether to output the auditing policy at end of cmdlet execution</span></span>

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

### <span data-ttu-id="ba9f1-162">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="ba9f1-162">-PredicateExpression</span></span>
<span data-ttu-id="ba9f1-163">A naplók szűréséhez használt T-SQL predikátum (WHERE záradék).</span><span class="sxs-lookup"><span data-stu-id="ba9f1-163">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="ba9f1-164">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba9f1-164">-ResourceGroupName</span></span>
<span data-ttu-id="ba9f1-165">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ba9f1-165">The name of the resource group.</span></span>

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

### <span data-ttu-id="ba9f1-166">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="ba9f1-166">-RetentionInDays</span></span>
<span data-ttu-id="ba9f1-167">A naplók retenciós napjainak száma.</span><span class="sxs-lookup"><span data-stu-id="ba9f1-167">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="ba9f1-168">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="ba9f1-168">-ServerName</span></span>
<span data-ttu-id="ba9f1-169">SQL-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="ba9f1-169">SQL server name.</span></span>

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

### <span data-ttu-id="ba9f1-170">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="ba9f1-170">-State</span></span>
<span data-ttu-id="ba9f1-171">A házirend állapota.</span><span class="sxs-lookup"><span data-stu-id="ba9f1-171">The state of the policy.</span></span>

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

### <span data-ttu-id="ba9f1-172">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ba9f1-172">-StorageAccountName</span></span>
<span data-ttu-id="ba9f1-173">A tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="ba9f1-173">The name of the storage account.</span></span>

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

### <span data-ttu-id="ba9f1-174">-StorageAccountSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ba9f1-174">-StorageAccountSubscriptionId</span></span>
<span data-ttu-id="ba9f1-175">A Storage Account előfizetés azonosítója</span><span class="sxs-lookup"><span data-stu-id="ba9f1-175">The storage account subscription id</span></span>

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

### <span data-ttu-id="ba9f1-176">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="ba9f1-176">-StorageKeyType</span></span>
<span data-ttu-id="ba9f1-177">Itt adhatja meg, hogy a tárterület-hozzáférési kulcsok közül melyik használható.</span><span class="sxs-lookup"><span data-stu-id="ba9f1-177">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="ba9f1-178">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="ba9f1-178">-WorkspaceResourceId</span></span>
<span data-ttu-id="ba9f1-179">A napló Analytics-munkaterületének erőforrás-azonosítója (log Analytics-munkaterületen), amelybe naplókat szeretne küldeni.</span><span class="sxs-lookup"><span data-stu-id="ba9f1-179">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Audit Logs.</span></span> <span data-ttu-id="ba9f1-180">Példa:/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span><span class="sxs-lookup"><span data-stu-id="ba9f1-180">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

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

### <span data-ttu-id="ba9f1-181">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ba9f1-181">-Confirm</span></span>
<span data-ttu-id="ba9f1-182">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ba9f1-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba9f1-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba9f1-183">-WhatIf</span></span>
<span data-ttu-id="ba9f1-184">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ba9f1-184">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ba9f1-185">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ba9f1-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba9f1-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba9f1-186">CommonParameters</span></span>
<span data-ttu-id="ba9f1-187">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ba9f1-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba9f1-188">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ba9f1-188">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba9f1-189">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ba9f1-189">INPUTS</span></span>

### <span data-ttu-id="ba9f1-190">System. String</span><span class="sxs-lookup"><span data-stu-id="ba9f1-190">System.String</span></span>

### <span data-ttu-id="ba9f1-191">Microsoft. Azure. Command. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="ba9f1-191">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="ba9f1-192">Microsoft. Azure. Command. SQL. könyvvizsgálat. Model. AuditActionGroups []</span><span class="sxs-lookup"><span data-stu-id="ba9f1-192">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span></span>

### <span data-ttu-id="ba9f1-193">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ba9f1-193">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="ba9f1-194">System. GUID</span><span class="sxs-lookup"><span data-stu-id="ba9f1-194">System.Guid</span></span>

### <span data-ttu-id="ba9f1-195">System. null ' 1 [[System. UInt32, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ba9f1-195">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="ba9f1-196">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ba9f1-196">OUTPUTS</span></span>

### <span data-ttu-id="ba9f1-197">Microsoft. Azure. Command. SQL. könyvvizsgálat. Model. ServerBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="ba9f1-197">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="ba9f1-198">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ba9f1-198">NOTES</span></span>

## <span data-ttu-id="ba9f1-199">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ba9f1-199">RELATED LINKS</span></span>
