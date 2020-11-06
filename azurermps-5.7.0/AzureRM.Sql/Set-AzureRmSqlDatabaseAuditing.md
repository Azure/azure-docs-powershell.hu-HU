---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabaseauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditing.md
ms.openlocfilehash: 5eedeea96f7c1c2491e7388734b51977cb0dd1c3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494289"
---
# <span data-ttu-id="d8d25-101">Set-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="d8d25-101">Set-AzureRmSqlDatabaseAuditing</span></span>

## <span data-ttu-id="d8d25-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d8d25-102">SYNOPSIS</span></span>
<span data-ttu-id="d8d25-103">Az Azure SQL-adatbázisok naplózási beállításainak módosítása</span><span class="sxs-lookup"><span data-stu-id="d8d25-103">Changes the auditing settings for an Azure SQL database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8d25-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d8d25-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseAuditing -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>]
 [-AuditAction <String[]>] [-StorageAccountName <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8d25-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d8d25-105">DESCRIPTION</span></span>
<span data-ttu-id="d8d25-106">A **set-AzureRmSqlDatabaseAuditing** parancsmag egy Azure SQL-adatbázis naplózási beállításait módosítja.</span><span class="sxs-lookup"><span data-stu-id="d8d25-106">The **Set-AzureRmSqlDatabaseAuditing** cmdlet changes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="d8d25-107">A parancsmag használatához a *ResourceGroupName* , a *kiszolgálónév* és a *databasename* paraméterrel keresse meg az adatbázist.</span><span class="sxs-lookup"><span data-stu-id="d8d25-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="d8d25-108">Adja meg a *StorageAccountName* paramétert a naplók tárolási fiókjának a megadásához, illetve a *StorageKeyType* paramétert a tárolási kulcsok meghatározásához.</span><span class="sxs-lookup"><span data-stu-id="d8d25-108">Specify the *StorageAccountName* parameter to specify the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span>
<span data-ttu-id="d8d25-109">A házirend engedélyezéséhez vagy letiltásához használja az *állami* paramétert.</span><span class="sxs-lookup"><span data-stu-id="d8d25-109">Use the *State* parameter to enable/disable the policy.</span></span>

<span data-ttu-id="d8d25-110">A naplók adatmegőrzését úgy is megadhatja, hogy az *RetentionInDays* paraméter értékét adja meg a naplók időszakának meghatározásához.</span><span class="sxs-lookup"><span data-stu-id="d8d25-110">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

<span data-ttu-id="d8d25-111">A parancsmag sikeres futtatása után az adatbázis naplózása engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="d8d25-111">After the cmdlet runs successfully, auditing of the database is enabled.</span></span>
<span data-ttu-id="d8d25-112">Ha a parancsmag sikerrel jár, és a *PassThru* paramétert használja, az adatbázis-azonosítók mellett egy olyan objektumot ad eredményül, amely leírja az aktuális blob-naplózási házirendet.</span><span class="sxs-lookup"><span data-stu-id="d8d25-112">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current blob auditing policy in addition to the database identifiers.</span></span>
<span data-ttu-id="d8d25-113">Az adatbázis-azonosítók közé tartoznak a következők: a **ResourceGroupName** , a **kiszolgálónév** és a **databasename**.</span><span class="sxs-lookup"><span data-stu-id="d8d25-113">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>

## <span data-ttu-id="d8d25-114">Példák</span><span class="sxs-lookup"><span data-stu-id="d8d25-114">EXAMPLES</span></span>

### <span data-ttu-id="d8d25-115">1. példa: az Azure SQL-adatbázisok naplózási házirendjének engedélyezése</span><span class="sxs-lookup"><span data-stu-id="d8d25-115">Example 1: Enable the auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01"
```

### <span data-ttu-id="d8d25-116">2. példa: az Azure SQL-adatbázisok blob-naplózási házirendjének letiltása</span><span class="sxs-lookup"><span data-stu-id="d8d25-116">Example 2: Disable the blob auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

## <span data-ttu-id="d8d25-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d8d25-117">PARAMETERS</span></span>

### <span data-ttu-id="d8d25-118">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="d8d25-118">-AuditAction</span></span>
<span data-ttu-id="d8d25-119">A naplózási műveletek halmaza.</span><span class="sxs-lookup"><span data-stu-id="d8d25-119">The set of audit actions.</span></span>  
<span data-ttu-id="d8d25-120">A naplózandó támogatott műveletek a következők:</span><span class="sxs-lookup"><span data-stu-id="d8d25-120">The supported actions to audit are:</span></span>  
<span data-ttu-id="d8d25-121">Válassza</span><span class="sxs-lookup"><span data-stu-id="d8d25-121">SELECT</span></span>  
<span data-ttu-id="d8d25-122">FRISSÍTÉS</span><span class="sxs-lookup"><span data-stu-id="d8d25-122">UPDATE</span></span>  
<span data-ttu-id="d8d25-123">BESZÚRÁSA</span><span class="sxs-lookup"><span data-stu-id="d8d25-123">INSERT</span></span>  
<span data-ttu-id="d8d25-124">TÖRLÉSE</span><span class="sxs-lookup"><span data-stu-id="d8d25-124">DELETE</span></span>  
<span data-ttu-id="d8d25-125">VÉGREHAJTÁSA</span><span class="sxs-lookup"><span data-stu-id="d8d25-125">EXECUTE</span></span>  
<span data-ttu-id="d8d25-126">KAP</span><span class="sxs-lookup"><span data-stu-id="d8d25-126">RECEIVE</span></span>  
<span data-ttu-id="d8d25-127">HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d8d25-127">REFERENCES</span></span>  

<span data-ttu-id="d8d25-128">A naplózandó műveletek meghatározására szolgáló általános űrlap:</span><span class="sxs-lookup"><span data-stu-id="d8d25-128">The general form for defining an action to be audited is:</span></span>

<span data-ttu-id="d8d25-129">cselekvési [Object] BY [megbízó]</span><span class="sxs-lookup"><span data-stu-id="d8d25-129">[action] ON [object] BY [principal]</span></span>

<span data-ttu-id="d8d25-130">Felhívjuk a figyelmét arra, hogy az [objektum] a fenti formátumban hivatkozhat egy objektumra, például táblázatra, nézetre vagy tárolt eljárásra, illetve egész adatbázisra vagy sémára.</span><span class="sxs-lookup"><span data-stu-id="d8d25-130">Note that [object] in the above format can refer to an object like a table, view, or stored procedure, or an entire database or schema.</span></span> <span data-ttu-id="d8d25-131">Az utóbbi esetekben az Forms DATABASE:: [dbname] és a SCHEMA:: [SchemaName] használatban van.</span><span class="sxs-lookup"><span data-stu-id="d8d25-131">For the latter cases, the forms DATABASE::[dbname] and SCHEMA::[schemaname] are used, respectively.</span></span>

<span data-ttu-id="d8d25-132">Példa:</span><span class="sxs-lookup"><span data-stu-id="d8d25-132">For example:</span></span>  
<span data-ttu-id="d8d25-133">Válassza a dbo. Táblanév nyilvánosak szerint lehetőséget</span><span class="sxs-lookup"><span data-stu-id="d8d25-133">SELECT on dbo.myTable by public</span></span>  
<span data-ttu-id="d8d25-134">Válassza az adatbázis: myDatabase nyilvánosak szerint lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="d8d25-134">SELECT on DATABASE::myDatabase by public</span></span>  
<span data-ttu-id="d8d25-135">SELECT on SCHEMA:: mySchema by Public</span><span class="sxs-lookup"><span data-stu-id="d8d25-135">SELECT on SCHEMA::mySchema by public</span></span>  

<span data-ttu-id="d8d25-136">További információ: https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions .</span><span class="sxs-lookup"><span data-stu-id="d8d25-136">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8d25-137">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="d8d25-137">-AuditActionGroup</span></span>
<span data-ttu-id="d8d25-138">A használni kívánt műveleti csoportok a következő kombinációk: Ez a művelet naplózza az adatbázissal végzett összes lekérdezést és tárolt eljárást, valamint a sikeres és sikertelen bejelentkezéseket:</span><span class="sxs-lookup"><span data-stu-id="d8d25-138">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="d8d25-139">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="d8d25-139">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="d8d25-140">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="d8d25-140">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="d8d25-141">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="d8d25-141">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  

<span data-ttu-id="d8d25-142">Ez a fenti kombináció egyben az alapértelmezés szerint konfigurált halmaz.</span><span class="sxs-lookup"><span data-stu-id="d8d25-142">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="d8d25-143">Ezek a csoportok az adatbázissal szemben végrehajtott összes SQL-utasítást és tárolt eljárást lefoglalják, és nem használhatók együtt más csoportokkal, mert ez a művelet duplikálja a naplókat.</span><span class="sxs-lookup"><span data-stu-id="d8d25-143">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="d8d25-144">További információ: https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="d8d25-144">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

```yaml
Type: AuditActionGroups[]
Parameter Sets: (All)
Aliases:
Accepted values: BATCH_STARTED_GROUP, BATCH_COMPLETED_GROUP, APPLICATION_ROLE_CHANGE_PASSWORD_GROUP, BACKUP_RESTORE_GROUP, DATABASE_LOGOUT_GROUP, DATABASE_OBJECT_CHANGE_GROUP, DATABASE_OBJECT_OWNERSHIP_CHANGE_GROUP, DATABASE_OBJECT_PERMISSION_CHANGE_GROUP, DATABASE_OPERATION_GROUP, AUDIT_CHANGE_GROUP, DATABASE_PERMISSION_CHANGE_GROUP, DATABASE_PRINCIPAL_CHANGE_GROUP, DATABASE_PRINCIPAL_IMPERSONATION_GROUP, DATABASE_ROLE_MEMBER_CHANGE_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, SCHEMA_OBJECT_ACCESS_GROUP, SCHEMA_OBJECT_CHANGE_GROUP, SCHEMA_OBJECT_OWNERSHIP_CHANGE_GROUP, SCHEMA_OBJECT_PERMISSION_CHANGE_GROUP, SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, USER_CHANGE_PASSWORD_GROUP

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8d25-145">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d8d25-145">-DatabaseName</span></span>
<span data-ttu-id="d8d25-146">SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="d8d25-146">SQL Database name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8d25-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8d25-147">-DefaultProfile</span></span>
<span data-ttu-id="d8d25-148">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d8d25-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8d25-149">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d8d25-149">-PassThru</span></span>
<span data-ttu-id="d8d25-150">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="d8d25-150">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8d25-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8d25-151">-ResourceGroupName</span></span>
<span data-ttu-id="d8d25-152">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d8d25-152">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8d25-153">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="d8d25-153">-RetentionInDays</span></span>
<span data-ttu-id="d8d25-154">A naplók retenciós napjainak száma.</span><span class="sxs-lookup"><span data-stu-id="d8d25-154">The number of retention days for the audit logs.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8d25-155">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="d8d25-155">-ServerName</span></span>
<span data-ttu-id="d8d25-156">SQL-adatbázis kiszolgálójának neve</span><span class="sxs-lookup"><span data-stu-id="d8d25-156">SQL Database server name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8d25-157">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="d8d25-157">-State</span></span>
<span data-ttu-id="d8d25-158">A házirend állapota.</span><span class="sxs-lookup"><span data-stu-id="d8d25-158">The state of the policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8d25-159">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d8d25-159">-StorageAccountName</span></span>
<span data-ttu-id="d8d25-160">A tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="d8d25-160">The name of the storage account.</span></span> <span data-ttu-id="d8d25-161">A helyettesítő karakterek nem engedélyezettek.</span><span class="sxs-lookup"><span data-stu-id="d8d25-161">Wildcard characters are not permitted.</span></span>  
<span data-ttu-id="d8d25-162">Ehhez a paraméterhez nincs szükség.</span><span class="sxs-lookup"><span data-stu-id="d8d25-162">This parameter is not required.</span></span>  
<span data-ttu-id="d8d25-163">Ha nem adja meg ezt a paramétert, a parancsmag a korábban a naplózási házirend részeként megadott tárolási fiókot használja.</span><span class="sxs-lookup"><span data-stu-id="d8d25-163">If you do not specify this parameter, the cmdlet uses the storage account that was defined previously as part of the auditing policy.</span></span>  
<span data-ttu-id="d8d25-164">Ha most először adja meg a naplózási házirendet, és nem adja meg ezt a paramétert, a parancsmag nem működik.</span><span class="sxs-lookup"><span data-stu-id="d8d25-164">If this is the first time an auditing policy is defined and you do not specify this parameter, the cmdlet fails.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8d25-165">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="d8d25-165">-StorageKeyType</span></span>
<span data-ttu-id="d8d25-166">Itt adhatja meg, hogy a tárterület-hozzáférési kulcsok közül melyik használható.</span><span class="sxs-lookup"><span data-stu-id="d8d25-166">Specifies which of the storage access keys to use.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8d25-167">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d8d25-167">-Confirm</span></span>
<span data-ttu-id="d8d25-168">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d8d25-168">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8d25-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8d25-169">-WhatIf</span></span>
<span data-ttu-id="d8d25-170">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d8d25-170">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d8d25-171">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d8d25-171">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8d25-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8d25-172">CommonParameters</span></span>
<span data-ttu-id="d8d25-173">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d8d25-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8d25-174">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8d25-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8d25-175">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d8d25-175">INPUTS</span></span>

### <span data-ttu-id="d8d25-176">Nincs</span><span class="sxs-lookup"><span data-stu-id="d8d25-176">None</span></span>
<span data-ttu-id="d8d25-177">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="d8d25-177">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d8d25-178">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d8d25-178">OUTPUTS</span></span>

### <span data-ttu-id="d8d25-179">Microsoft. Azure. Command. SQL. Security. Model. DatabaseBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="d8d25-179">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="d8d25-180">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d8d25-180">NOTES</span></span>

## <span data-ttu-id="d8d25-181">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d8d25-181">RELATED LINKS</span></span>
