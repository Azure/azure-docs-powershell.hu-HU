---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditing.md
ms.openlocfilehash: 80887d1c3cfc91c9eba23f686deac071660cf852
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501015"
---
# <span data-ttu-id="24ce9-101">Set-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="24ce9-101">Set-AzureRmSqlServerAuditing</span></span>

## <span data-ttu-id="24ce9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="24ce9-102">SYNOPSIS</span></span>
<span data-ttu-id="24ce9-103">Az Azure SQL Server-kiszolgálók naplózási beállításainak módosítása</span><span class="sxs-lookup"><span data-stu-id="24ce9-103">Changes the auditing settings of an Azure SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24ce9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="24ce9-104">SYNTAX</span></span>

### <span data-ttu-id="24ce9-105">DefaultParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="24ce9-105">DefaultParameterSet (Default)</span></span>
```
Set-AzureRmSqlServerAuditing -State <String> [-AuditActionGroup <AuditActionGroups[]>] [-PassThru]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-PredicateExpression <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24ce9-106">StorageAccountSubscriptionIdSet</span><span class="sxs-lookup"><span data-stu-id="24ce9-106">StorageAccountSubscriptionIdSet</span></span>
```
Set-AzureRmSqlServerAuditing -State <String> [-AuditActionGroup <AuditActionGroups[]>] [-PassThru]
 -StorageAccountName <String> [-StorageAccountSubscriptionId <Guid>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-PredicateExpression <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="24ce9-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="24ce9-107">DESCRIPTION</span></span>
<span data-ttu-id="24ce9-108">A **set-AzureRmSqlServerAuditing** parancsmag az Azure SQL Server-kiszolgálók naplózási beállításait módosítja.</span><span class="sxs-lookup"><span data-stu-id="24ce9-108">The **Set-AzureRmSqlServerAuditing** cmdlet changes the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="24ce9-109">A parancsmag használatához a *ResourceGroupName* és a *kiszolgálónév* paraméterrel keresse meg a kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="24ce9-109">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="24ce9-110">Adja meg a *StorageAccountName* paramétert a naplók tárolási fiókjának a megadásához, illetve a *StorageKeyType* paramétert a tárolási kulcsok meghatározásához.</span><span class="sxs-lookup"><span data-stu-id="24ce9-110">Specify the *StorageAccountName* parameter to specify the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span>
<span data-ttu-id="24ce9-111">A házirend engedélyezéséhez vagy letiltásához használja az *állami* paramétert.</span><span class="sxs-lookup"><span data-stu-id="24ce9-111">Use the *State* parameter to enable/disable the policy.</span></span>
<span data-ttu-id="24ce9-112">A naplók adatmegőrzését úgy is megadhatja, hogy az *RetentionInDays* paraméter értékét adja meg a naplók időszakának meghatározásához.</span><span class="sxs-lookup"><span data-stu-id="24ce9-112">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>
<span data-ttu-id="24ce9-113">A parancsmag sikeres futtatását követően a megadott Azure SQL-kiszolgálón megadott Azure SQL-adatbázisok naplózása engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="24ce9-113">After the cmdlet runs successfully, auditing of the Azure SQL databases that are defined in the specified Azure SQL server is enabled.</span></span>
<span data-ttu-id="24ce9-114">Ha a parancsmag sikerrel jár, és a *PassThru* paramétert használja, a kiszolgálói azonosítók mellett egy olyan objektumot ad eredményül, amely leírja az aktuális blob-naplózási házirendet.</span><span class="sxs-lookup"><span data-stu-id="24ce9-114">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current blob auditing policy in addition to the server identifiers.</span></span>
<span data-ttu-id="24ce9-115">A kiszolgálói azonosítók tartalmazzák, de nem korlátozódnak a **ResourceGroupName** és a **kiszolgáló_neve** -ra.</span><span class="sxs-lookup"><span data-stu-id="24ce9-115">Server identifiers include, but are not limited to, **ResourceGroupName** and **ServerName**.</span></span>

## <span data-ttu-id="24ce9-116">Példák</span><span class="sxs-lookup"><span data-stu-id="24ce9-116">EXAMPLES</span></span>

### <span data-ttu-id="24ce9-117">1. példa: az Azure SQL Server-kiszolgálók naplózási házirendjének engedélyezése</span><span class="sxs-lookup"><span data-stu-id="24ce9-117">Example 1: Enable the auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22"
```

### <span data-ttu-id="24ce9-118">2. példa: az Azure SQL Server-kiszolgálók naplózási házirendjének letiltása</span><span class="sxs-lookup"><span data-stu-id="24ce9-118">Example 2: Disable the auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

### <span data-ttu-id="24ce9-119">3. példa: az Azure SQL Server-kiszolgálók naplózási házirendjének engedélyezése másik előfizetésből származó tárolási fiók használatával</span><span class="sxs-lookup"><span data-stu-id="24ce9-119">Example 3: Enable the auditing policy of an Azure SQL server using a storage account from a different subscription</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -StorageAccountSubscriptionId "7fe3301d-31d3-4668-af5e-211a890ba6e3"
```

### <span data-ttu-id="24ce9-120">Példa 4: az Azure SQL-adatbázisok kiterjesztett naplózási házirendjének engedélyezése</span><span class="sxs-lookup"><span data-stu-id="24ce9-120">Example 4: Enable the extended auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01" -PredicateExpression "statement <> 'select 1'"
```

### <span data-ttu-id="24ce9-121">Példa 5: az Azure SQL-adatbázisok kiterjesztett naplózási házirendjének eltávolítása, és nem a naplózási házirend beállítása.</span><span class="sxs-lookup"><span data-stu-id="24ce9-121">Example 5: Remove the extended auditing policy of an Azure SQL database, and set an auditing policy instead of it.</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01" -PredicateExpression ""
```

## <span data-ttu-id="24ce9-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="24ce9-122">PARAMETERS</span></span>

### <span data-ttu-id="24ce9-123">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="24ce9-123">-AuditActionGroup</span></span>
<span data-ttu-id="24ce9-124">A használni kívánt műveleti csoportok a következő kombinációk: Ez a művelet az adatbázissal végrehajtott összes lekérdezést és tárolt eljárást naplózza, valamint a sikeres és sikertelen bejelentkezéseket: "BATCH_COMPLETED_GROUP", "SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP", "FAILED_DATABASE_AUTHENTICATION_GROUP" Ez a fenti kombináció is az alapértelmezés szerint konfigurált beállítás.</span><span class="sxs-lookup"><span data-stu-id="24ce9-124">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins: "BATCH_COMPLETED_GROUP", "SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP", "FAILED_DATABASE_AUTHENTICATION_GROUP" This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="24ce9-125">Ezek a csoportok az adatbázissal szemben végrehajtott összes SQL-utasítást és tárolt eljárást lefoglalják, és nem használhatók együtt más csoportokkal, mert ez a művelet duplikálja a naplókat.</span><span class="sxs-lookup"><span data-stu-id="24ce9-125">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span> <span data-ttu-id="24ce9-126">További információ: https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="24ce9-126">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="24ce9-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24ce9-127">-DefaultProfile</span></span>
<span data-ttu-id="24ce9-128">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="24ce9-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24ce9-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="24ce9-129">-PassThru</span></span>
<span data-ttu-id="24ce9-130">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="24ce9-130">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="24ce9-131">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="24ce9-131">-PredicateExpression</span></span>
<span data-ttu-id="24ce9-132">A naplók szűréséhez használt WHERE záradék nyilatkozata.</span><span class="sxs-lookup"><span data-stu-id="24ce9-132">The statement of the Where Clause used to filter audit logs.</span></span>

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

### <span data-ttu-id="24ce9-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24ce9-133">-ResourceGroupName</span></span>
<span data-ttu-id="24ce9-134">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="24ce9-134">The name of the resource group.</span></span>

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

### <span data-ttu-id="24ce9-135">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="24ce9-135">-RetentionInDays</span></span>
<span data-ttu-id="24ce9-136">A naplók retenciós napjainak száma.</span><span class="sxs-lookup"><span data-stu-id="24ce9-136">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="24ce9-137">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="24ce9-137">-ServerName</span></span>
<span data-ttu-id="24ce9-138">SQL-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="24ce9-138">SQL server name.</span></span>

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

### <span data-ttu-id="24ce9-139">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="24ce9-139">-State</span></span>
<span data-ttu-id="24ce9-140">A házirend állapota.</span><span class="sxs-lookup"><span data-stu-id="24ce9-140">The state of the policy.</span></span>

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

### <span data-ttu-id="24ce9-141">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="24ce9-141">-StorageAccountName</span></span>
<span data-ttu-id="24ce9-142">A tárolási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="24ce9-142">The name of the storage account.</span></span> <span data-ttu-id="24ce9-143">A helyettesítő karakterek nem engedélyezettek.</span><span class="sxs-lookup"><span data-stu-id="24ce9-143">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="24ce9-144">Ehhez a paraméterhez nincs szükség.</span><span class="sxs-lookup"><span data-stu-id="24ce9-144">This parameter is not required.</span></span>
<span data-ttu-id="24ce9-145">Ha nem adja meg ezt a paramétert, a parancsmag a korábban a naplózási házirend részeként megadott tárolási fiókot használja.</span><span class="sxs-lookup"><span data-stu-id="24ce9-145">If you do not specify this parameter, the cmdlet uses the storage account that was defined previously as part of the auditing policy.</span></span>
<span data-ttu-id="24ce9-146">Ha most először adja meg a naplózási házirendet, és nem adja meg ezt a paramétert, a parancsmag nem működik.</span><span class="sxs-lookup"><span data-stu-id="24ce9-146">If this is the first time an auditing policy is defined and you do not specify this parameter, the cmdlet fails.</span></span>

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

### <span data-ttu-id="24ce9-147">-StorageAccountSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="24ce9-147">-StorageAccountSubscriptionId</span></span>
<span data-ttu-id="24ce9-148">A tárolási fiók előfizetési azonosítóját adja meg</span><span class="sxs-lookup"><span data-stu-id="24ce9-148">Specifies storage account subscription id</span></span>

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

### <span data-ttu-id="24ce9-149">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="24ce9-149">-StorageKeyType</span></span>
<span data-ttu-id="24ce9-150">Itt adhatja meg, hogy a tárterület-hozzáférési kulcsok közül melyik használható.</span><span class="sxs-lookup"><span data-stu-id="24ce9-150">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="24ce9-151">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="24ce9-151">-Confirm</span></span>
<span data-ttu-id="24ce9-152">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="24ce9-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24ce9-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24ce9-153">-WhatIf</span></span>
<span data-ttu-id="24ce9-154">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="24ce9-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="24ce9-155">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="24ce9-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24ce9-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24ce9-156">CommonParameters</span></span>
<span data-ttu-id="24ce9-157">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="24ce9-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24ce9-158">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24ce9-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24ce9-159">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="24ce9-159">INPUTS</span></span>

## <span data-ttu-id="24ce9-160">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="24ce9-160">OUTPUTS</span></span>

## <span data-ttu-id="24ce9-161">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="24ce9-161">NOTES</span></span>

## <span data-ttu-id="24ce9-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="24ce9-162">RELATED LINKS</span></span>
