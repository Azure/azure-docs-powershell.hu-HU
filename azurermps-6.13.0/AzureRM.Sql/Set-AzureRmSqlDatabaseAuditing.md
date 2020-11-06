---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabaseauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditing.md
ms.openlocfilehash: e28295a5f743e1475075e93a52c21bba8bd83e08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493609"
---
# <span data-ttu-id="ad96d-101">Set-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="ad96d-101">Set-AzureRmSqlDatabaseAuditing</span></span>

## <span data-ttu-id="ad96d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ad96d-102">SYNOPSIS</span></span>
<span data-ttu-id="ad96d-103">Az Azure SQL-adatbázisok naplózási beállításainak módosítása</span><span class="sxs-lookup"><span data-stu-id="ad96d-103">Changes the auditing settings for an Azure SQL database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad96d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ad96d-104">SYNTAX</span></span>

### <span data-ttu-id="ad96d-105">DefaultParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ad96d-105">DefaultParameterSet (Default)</span></span>
```
Set-AzureRmSqlDatabaseAuditing -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>]
 [-AuditAction <String[]>] [-StorageAccountName <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-PredicateExpression <String>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ad96d-106">StorageAccountSubscriptionIdSet</span><span class="sxs-lookup"><span data-stu-id="ad96d-106">StorageAccountSubscriptionIdSet</span></span>
```
Set-AzureRmSqlDatabaseAuditing -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>]
 [-AuditAction <String[]>] -StorageAccountName <String> [-StorageAccountSubscriptionId <Guid>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-PredicateExpression <String>] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad96d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ad96d-107">DESCRIPTION</span></span>
<span data-ttu-id="ad96d-108">A **set-AzureRmSqlDatabaseAuditing** parancsmag egy Azure SQL-adatbázis naplózási beállításait módosítja.</span><span class="sxs-lookup"><span data-stu-id="ad96d-108">The **Set-AzureRmSqlDatabaseAuditing** cmdlet changes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="ad96d-109">A parancsmag használatához a *ResourceGroupName* , a *kiszolgálónév* és a *databasename* paraméterrel keresse meg az adatbázist.</span><span class="sxs-lookup"><span data-stu-id="ad96d-109">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="ad96d-110">Adja meg a *StorageAccountName* paramétert a naplók tárolási fiókjának a megadásához, illetve a *StorageKeyType* paramétert a tárolási kulcsok meghatározásához.</span><span class="sxs-lookup"><span data-stu-id="ad96d-110">Specify the *StorageAccountName* parameter to specify the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span>
<span data-ttu-id="ad96d-111">A házirend engedélyezéséhez vagy letiltásához használja az *állami* paramétert.</span><span class="sxs-lookup"><span data-stu-id="ad96d-111">Use the *State* parameter to enable/disable the policy.</span></span>
<span data-ttu-id="ad96d-112">A naplók adatmegőrzését úgy is megadhatja, hogy az *RetentionInDays* paraméter értékét adja meg a naplók időszakának meghatározásához.</span><span class="sxs-lookup"><span data-stu-id="ad96d-112">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>
<span data-ttu-id="ad96d-113">A parancsmag sikeres futtatása után az adatbázis naplózása engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="ad96d-113">After the cmdlet runs successfully, auditing of the database is enabled.</span></span>
<span data-ttu-id="ad96d-114">Ha a parancsmag sikerrel jár, és a *PassThru* paramétert használja, az adatbázis-azonosítók mellett egy olyan objektumot ad eredményül, amely leírja az aktuális blob-naplózási házirendet.</span><span class="sxs-lookup"><span data-stu-id="ad96d-114">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current blob auditing policy in addition to the database identifiers.</span></span>
<span data-ttu-id="ad96d-115">Az adatbázis-azonosítók közé tartoznak a következők: a **ResourceGroupName** , a **kiszolgálónév** és a **databasename**.</span><span class="sxs-lookup"><span data-stu-id="ad96d-115">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>

## <span data-ttu-id="ad96d-116">Példák</span><span class="sxs-lookup"><span data-stu-id="ad96d-116">EXAMPLES</span></span>

### <span data-ttu-id="ad96d-117">1. példa: az Azure SQL-adatbázisok naplózási házirendjének engedélyezése</span><span class="sxs-lookup"><span data-stu-id="ad96d-117">Example 1: Enable the auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01"
```

### <span data-ttu-id="ad96d-118">2. példa: az Azure SQL-adatbázisok blob-naplózási házirendjének letiltása</span><span class="sxs-lookup"><span data-stu-id="ad96d-118">Example 2: Disable the blob auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

### <span data-ttu-id="ad96d-119">3. példa: az Azure SQL-adatbázisok naplózási házirendjének engedélyezése egy másik előfizetésből származó tárolási fiók használatával</span><span class="sxs-lookup"><span data-stu-id="ad96d-119">Example 3: Enable the auditing policy of an Azure SQL database using a storage account from a different subscription</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -StorageAccountSubscriptionId "7fe3301d-31d3-4668-af5e-211a890ba6e3"
```

### <span data-ttu-id="ad96d-120">Példa 4: az Azure SQL-adatbázisok kiterjesztett naplózási házirendjének engedélyezése</span><span class="sxs-lookup"><span data-stu-id="ad96d-120">Example 4: Enable the extended auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01" -PredicateExpression "statement <> 'select 1'"
```

### <span data-ttu-id="ad96d-121">Példa 5: az Azure SQL-adatbázisok kiterjesztett naplózási házirendjének eltávolítása, és nem a naplózási házirend beállítása.</span><span class="sxs-lookup"><span data-stu-id="ad96d-121">Example 5: Remove the extended auditing policy of an Azure SQL database, and set an auditing policy instead of it.</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01" -PredicateExpression ""
```

## <span data-ttu-id="ad96d-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ad96d-122">PARAMETERS</span></span>

### <span data-ttu-id="ad96d-123">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="ad96d-123">-AuditAction</span></span>
<span data-ttu-id="ad96d-124">A naplózási műveletek halmaza.</span><span class="sxs-lookup"><span data-stu-id="ad96d-124">The set of audit actions.</span></span>
<span data-ttu-id="ad96d-125">A naplózandó támogatott műveletek a következők: válassza a frissítés beszúrása a következőre: a küldési műveletek törlése hivatkozás a naplózandó művelet meghatározásának általános űrlapja: [művelet] a [Object] ON [Principal] megjegyzés szerint az [objektum] a fenti formátumban hivatkozhat egy objektumra, például táblázatra, nézetre vagy tárolt eljárásra, illetve egész adatbázisra vagy sémára.</span><span class="sxs-lookup"><span data-stu-id="ad96d-125">The supported actions to audit are: SELECT UPDATE INSERT DELETE EXECUTE RECEIVE REFERENCES The general form for defining an action to be audited is: [action] ON [object] BY [principal] Note that [object] in the above format can refer to an object like a table, view, or stored procedure, or an entire database or schema.</span></span> <span data-ttu-id="ad96d-126">Az utóbbi esetekben az Forms DATABASE:: [dbname] és a SCHEMA:: [SchemaName] használatban van.</span><span class="sxs-lookup"><span data-stu-id="ad96d-126">For the latter cases, the forms DATABASE::[dbname] and SCHEMA::[schemaname] are used, respectively.</span></span>
<span data-ttu-id="ad96d-127">Például: SELECT on dbo. Táblanév by Public SELECT on DATABASE:: myDatabase by Public SELECT on SCHEMA:: mySchema by Public további információért lásd: https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions .</span><span class="sxs-lookup"><span data-stu-id="ad96d-127">For example: SELECT on dbo.myTable by public SELECT on DATABASE::myDatabase by public SELECT on SCHEMA::mySchema by public For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions.</span></span>

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

### <span data-ttu-id="ad96d-128">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="ad96d-128">-AuditActionGroup</span></span>
<span data-ttu-id="ad96d-129">A használni kívánt műveleti csoportok a következő kombinációk: Ez a művelet az adatbázissal végrehajtott összes lekérdezést és tárolt eljárást naplózza, valamint a sikeres és sikertelen bejelentkezéseket: "BATCH_COMPLETED_GROUP", "SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP", "FAILED_DATABASE_AUTHENTICATION_GROUP" Ez a fenti kombináció is az alapértelmezés szerint konfigurált beállítás.</span><span class="sxs-lookup"><span data-stu-id="ad96d-129">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins: "BATCH_COMPLETED_GROUP", "SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP", "FAILED_DATABASE_AUTHENTICATION_GROUP" This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="ad96d-130">Ezek a csoportok az adatbázissal szemben végrehajtott összes SQL-utasítást és tárolt eljárást lefoglalják, és nem használhatók együtt más csoportokkal, mert ez a művelet duplikálja a naplókat.</span><span class="sxs-lookup"><span data-stu-id="ad96d-130">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span> <span data-ttu-id="ad96d-131">További információ: https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="ad96d-131">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]
Parameter Sets: (All)
Aliases:
Accepted values: BATCH_STARTED_GROUP, BATCH_COMPLETED_GROUP, APPLICATION_ROLE_CHANGE_PASSWORD_GROUP, BACKUP_RESTORE_GROUP, DATABASE_LOGOUT_GROUP, DATABASE_OBJECT_CHANGE_GROUP, DATABASE_OBJECT_OWNERSHIP_CHANGE_GROUP, DATABASE_OBJECT_PERMISSION_CHANGE_GROUP, DATABASE_OPERATION_GROUP, AUDIT_CHANGE_GROUP, DATABASE_PERMISSION_CHANGE_GROUP, DATABASE_PRINCIPAL_CHANGE_GROUP, DATABASE_PRINCIPAL_IMPERSONATION_GROUP, DATABASE_ROLE_MEMBER_CHANGE_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, SCHEMA_OBJECT_ACCESS_GROUP, SCHEMA_OBJECT_CHANGE_GROUP, SCHEMA_OBJECT_OWNERSHIP_CHANGE_GROUP, SCHEMA_OBJECT_PERMISSION_CHANGE_GROUP, SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, USER_CHANGE_PASSWORD_GROUP

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad96d-132">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ad96d-132">-DatabaseName</span></span>
<span data-ttu-id="ad96d-133">SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="ad96d-133">SQL Database name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad96d-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad96d-134">-DefaultProfile</span></span>
<span data-ttu-id="ad96d-135">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ad96d-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad96d-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ad96d-136">-PassThru</span></span>
<span data-ttu-id="ad96d-137">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="ad96d-137">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad96d-138">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="ad96d-138">-PredicateExpression</span></span>
<span data-ttu-id="ad96d-139">A naplók szűréséhez használt WHERE záradék nyilatkozata.</span><span class="sxs-lookup"><span data-stu-id="ad96d-139">The statement of the Where Clause used to filter audit logs.</span></span>

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

### <span data-ttu-id="ad96d-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad96d-140">-ResourceGroupName</span></span>
<span data-ttu-id="ad96d-141">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ad96d-141">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad96d-142">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="ad96d-142">-RetentionInDays</span></span>
<span data-ttu-id="ad96d-143">A naplók retenciós napjainak száma.</span><span class="sxs-lookup"><span data-stu-id="ad96d-143">The number of retention days for the audit logs.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad96d-144">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="ad96d-144">-ServerName</span></span>
<span data-ttu-id="ad96d-145">SQL-adatbázis kiszolgálójának neve</span><span class="sxs-lookup"><span data-stu-id="ad96d-145">SQL Database server name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad96d-146">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="ad96d-146">-State</span></span>
<span data-ttu-id="ad96d-147">A házirend állapota.</span><span class="sxs-lookup"><span data-stu-id="ad96d-147">The state of the policy.</span></span>

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

### <span data-ttu-id="ad96d-148">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ad96d-148">-StorageAccountName</span></span>
<span data-ttu-id="ad96d-149">A tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="ad96d-149">The name of the storage account.</span></span> <span data-ttu-id="ad96d-150">A helyettesítő karakterek nem engedélyezettek.</span><span class="sxs-lookup"><span data-stu-id="ad96d-150">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="ad96d-151">Ehhez a paraméterhez nincs szükség.</span><span class="sxs-lookup"><span data-stu-id="ad96d-151">This parameter is not required.</span></span>
<span data-ttu-id="ad96d-152">Ha nem adja meg ezt a paramétert, a parancsmag a korábban a naplózási házirend részeként megadott tárolási fiókot használja.</span><span class="sxs-lookup"><span data-stu-id="ad96d-152">If you do not specify this parameter, the cmdlet uses the storage account that was defined previously as part of the auditing policy.</span></span>
<span data-ttu-id="ad96d-153">Ha most először adja meg a naplózási házirendet, és nem adja meg ezt a paramétert, a parancsmag nem működik.</span><span class="sxs-lookup"><span data-stu-id="ad96d-153">If this is the first time an auditing policy is defined and you do not specify this parameter, the cmdlet fails.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: StorageAccountSubscriptionIdSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad96d-154">-StorageAccountSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ad96d-154">-StorageAccountSubscriptionId</span></span>
<span data-ttu-id="ad96d-155">A tárolási fiók előfizetési azonosítóját adja meg</span><span class="sxs-lookup"><span data-stu-id="ad96d-155">Specifies storage account subscription id</span></span>

```yaml
Type: System.Guid
Parameter Sets: StorageAccountSubscriptionIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad96d-156">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="ad96d-156">-StorageKeyType</span></span>
<span data-ttu-id="ad96d-157">Itt adhatja meg, hogy a tárterület-hozzáférési kulcsok közül melyik használható.</span><span class="sxs-lookup"><span data-stu-id="ad96d-157">Specifies which of the storage access keys to use.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad96d-158">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ad96d-158">-Confirm</span></span>
<span data-ttu-id="ad96d-159">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ad96d-159">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad96d-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad96d-160">-WhatIf</span></span>
<span data-ttu-id="ad96d-161">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ad96d-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ad96d-162">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ad96d-162">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad96d-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad96d-163">CommonParameters</span></span>
<span data-ttu-id="ad96d-164">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ad96d-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad96d-165">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad96d-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad96d-166">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ad96d-166">INPUTS</span></span>

## <span data-ttu-id="ad96d-167">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ad96d-167">OUTPUTS</span></span>

## <span data-ttu-id="ad96d-168">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ad96d-168">NOTES</span></span>

## <span data-ttu-id="ad96d-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ad96d-169">RELATED LINKS</span></span>
