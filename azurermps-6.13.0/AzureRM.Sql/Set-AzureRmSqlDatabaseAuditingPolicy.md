---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabaseauditingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditingPolicy.md
ms.openlocfilehash: a9f0f2e478e94b45349efe85c6de643b5003a361
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493607"
---
# <span data-ttu-id="45d33-101">Set-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="45d33-101">Set-AzureRmSqlDatabaseAuditingPolicy</span></span>

## <span data-ttu-id="45d33-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="45d33-102">SYNOPSIS</span></span>
<span data-ttu-id="45d33-103">Az adatbázis naplózási házirendjének beállítása.</span><span class="sxs-lookup"><span data-stu-id="45d33-103">Sets the auditing policy for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45d33-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="45d33-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseAuditingPolicy [-AuditType <AuditType>] [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-EventType <String[]>]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-TableIdentifier <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45d33-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="45d33-105">DESCRIPTION</span></span>
<span data-ttu-id="45d33-106">A **set-AzureRmSqlDatabaseAuditingPolicy** parancsmag egy Azure SQL-adatbázis naplózási házirendjét módosítja.</span><span class="sxs-lookup"><span data-stu-id="45d33-106">The **Set-AzureRmSqlDatabaseAuditingPolicy** cmdlet changes the auditing policy of an Azure SQL database.</span></span>
<span data-ttu-id="45d33-107">A parancsmag használatához a *ResourceGroupName* , a *kiszolgálónév* és a *databasename* paraméterrel keresse meg az adatbázist.</span><span class="sxs-lookup"><span data-stu-id="45d33-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="45d33-108">Adja meg a *StorageAccountName* paramétert a naplók tárolási fiókjának a megadásához, illetve a *StorageKeyType* paramétert a tárolási kulcsok meghatározásához.</span><span class="sxs-lookup"><span data-stu-id="45d33-108">Specify the *StorageAccountName* parameter to specify the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span>
<span data-ttu-id="45d33-109">Azt is megadhatja, hogy az *RetentionInDays* és a *TableIdentifier* paramétereinek értéke megadásával meghatározza a naplózási naplók tábla adatmegőrzési listáját.</span><span class="sxs-lookup"><span data-stu-id="45d33-109">You can also define retention for the audit logs table by setting the value of the *RetentionInDays* and *TableIdentifier* parameters to define the period and the seed for the audit log table names.</span></span>
<span data-ttu-id="45d33-110">Adja meg a *EventType* paramétert annak meghatározásához, hogy milyen típusú események legyenek naplózva.</span><span class="sxs-lookup"><span data-stu-id="45d33-110">Specify the *EventType* parameter to define which event types to audit.</span></span>
<span data-ttu-id="45d33-111">A parancsmag sikeres futtatása után az adatbázis naplózása engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="45d33-111">After the cmdlet runs successfully, auditing of the database is enabled.</span></span>
<span data-ttu-id="45d33-112">Ha a táblázat naplózása, ha az adatbázis a kiszolgálójának házirendjét használta a naplózás megkezdése előtt, a naplózás leállítja a házirend használatát.</span><span class="sxs-lookup"><span data-stu-id="45d33-112">For Table Auditing, if the database used the policy of its server for auditing before you ran this cmdlet, auditing stops using that policy.</span></span> <span data-ttu-id="45d33-113">BLOB-naplózás esetén, ha az adatbázis a kiszolgálójának házirendjét használta naplózásra, mielőtt ezt a parancsmagot futtatta, a naplózási házirendek egymás mellett jelennek meg.</span><span class="sxs-lookup"><span data-stu-id="45d33-113">For Blob Auditing, if the database used the policy of its server for auditing before you ran this cmdlet, both auditing policies will exist side-by-side.</span></span>
<span data-ttu-id="45d33-114">Ha a parancsmag sikerrel jár, és a *PassThru* paramétert használja, az adatbázis-azonosítók mellett az aktuális naplózási házirendet leíró objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="45d33-114">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current auditing policy in addition to the database identifiers.</span></span>
<span data-ttu-id="45d33-115">Az adatbázis-azonosítók közé tartoznak a következők: a **ResourceGroupName** , a **kiszolgálónév** és a **databasename**.</span><span class="sxs-lookup"><span data-stu-id="45d33-115">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>
<span data-ttu-id="45d33-116">Ezt a parancsmagot az SQL Server stretch Database szolgáltatása is támogatja az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="45d33-116">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="45d33-117">Példák</span><span class="sxs-lookup"><span data-stu-id="45d33-117">EXAMPLES</span></span>

### <span data-ttu-id="45d33-118">Példa 1: az adatbázis naplózási házirendjének beállítása táblázat-naplózás használatára</span><span class="sxs-lookup"><span data-stu-id="45d33-118">Example 1: Set the auditing policy of a database to use Table auditing</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -AuditType Table -StorageAccountName "Storage31"
```

<span data-ttu-id="45d33-119">Ez a parancs a Server01 nevű Database01 nevű adatbázis naplózási házirendjét a Storage31 nevű tárolási fiók használatára állítja be.</span><span class="sxs-lookup"><span data-stu-id="45d33-119">This command sets the auditing policy of database named Database01 located on Server01 to use the storage account named Storage31.</span></span>

### <span data-ttu-id="45d33-120">2. példa: az adatbázis meglévő naplózási házirendjének a Storage Account (tárterület) kulcsának beállítása</span><span class="sxs-lookup"><span data-stu-id="45d33-120">Example 2: Set the storage account key of an existing auditing policy of a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -StorageAccountKey Secondary
```

<span data-ttu-id="45d33-121">Ez a parancs a Server01 található Database01 nevű adatbázis naplózási házirendjét úgy állítja be, hogy ugyanazt a tárolási fióknevet használja, de most már használja a másodlagos kulcsot.</span><span class="sxs-lookup"><span data-stu-id="45d33-121">This command sets the auditing policy of database named Database01 located on Server01 to keep using the same storage account name but to now use the secondary key.</span></span>

### <span data-ttu-id="45d33-122">3. példa: egy adatbázis naplózási házirendjének beállítása adott eseménytípus használatához</span><span class="sxs-lookup"><span data-stu-id="45d33-122">Example 3: Set the auditing policy of a database to use a specific event type</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -EventType Login_Failure
```

### <span data-ttu-id="45d33-123">Példa 4: az adatbázis naplózási házirendjének beállítása blob-naplózás használatára</span><span class="sxs-lookup"><span data-stu-id="45d33-123">Example 4: Set the auditing policy of a database to use Blob auditing</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -AuditType Blob -StorageAccountName "Storage31" -AuditActionGroup "SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP", "FAILED_DATABASE_AUTHENTICATION_GROUP" -AuditAction "UPDATE ON database::[Database01] BY [public]"  -RetentionInDays 8
```

<span data-ttu-id="45d33-124">Ez a parancs a Server01 található Database01 nevű adatbázis naplózási házirendjét állítja be.</span><span class="sxs-lookup"><span data-stu-id="45d33-124">This command sets the auditing policy of database named Database01 located on Server01.</span></span>
<span data-ttu-id="45d33-125">A házirend naplózza a Login_Failure eseménytípus típusát.</span><span class="sxs-lookup"><span data-stu-id="45d33-125">The policy logs the Login_Failure event type.</span></span>
<span data-ttu-id="45d33-126">A parancs nem módosítja a tárolási beállításokat.</span><span class="sxs-lookup"><span data-stu-id="45d33-126">The command does not change the storage settings.</span></span>

## <span data-ttu-id="45d33-127">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="45d33-127">PARAMETERS</span></span>

### <span data-ttu-id="45d33-128">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="45d33-128">-AuditAction</span></span>
<span data-ttu-id="45d33-129">Adjon meg egy vagy több naplózási műveletet.</span><span class="sxs-lookup"><span data-stu-id="45d33-129">Specify one or more audit actions.</span></span>
<span data-ttu-id="45d33-130">Ez a paraméter csak a blob-naplózásra érvényes.</span><span class="sxs-lookup"><span data-stu-id="45d33-130">This parameter is only applicable to Blob auditing.</span></span>

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

### <span data-ttu-id="45d33-131">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="45d33-131">-AuditActionGroup</span></span>
<span data-ttu-id="45d33-132">Adjon meg egy vagy több naplózási műveleti csoportot.</span><span class="sxs-lookup"><span data-stu-id="45d33-132">Specify one or more audit action groups.</span></span>
<span data-ttu-id="45d33-133">Ez a paraméter csak a blob-naplózásra érvényes.</span><span class="sxs-lookup"><span data-stu-id="45d33-133">This parameter is only applicable to Blob auditing.</span></span>

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

### <span data-ttu-id="45d33-134">-AuditType</span><span class="sxs-lookup"><span data-stu-id="45d33-134">-AuditType</span></span>
```yaml
Type: Microsoft.Azure.Commands.Sql.Auditing.Model.AuditType
Parameter Sets: (All)
Aliases:
Accepted values: NotSet, Table, Blob

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45d33-135">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="45d33-135">-DatabaseName</span></span>
<span data-ttu-id="45d33-136">Az adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="45d33-136">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="45d33-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45d33-137">-DefaultProfile</span></span>
<span data-ttu-id="45d33-138">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="45d33-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="45d33-139">-EventType</span><span class="sxs-lookup"><span data-stu-id="45d33-139">-EventType</span></span>
<span data-ttu-id="45d33-140">A naplózni kívánt esemény típusait adja meg.</span><span class="sxs-lookup"><span data-stu-id="45d33-140">Specifies the event types to audit.</span></span>
<span data-ttu-id="45d33-141">Ez a paraméter csak a tábla naplózására érvényes.</span><span class="sxs-lookup"><span data-stu-id="45d33-141">This parameter is only applicable to Table auditing.</span></span>
<span data-ttu-id="45d33-142">Több eseménytípus is megadható.</span><span class="sxs-lookup"><span data-stu-id="45d33-142">You can specify several event types.</span></span>
<span data-ttu-id="45d33-143">A mind lehetőséget megadhatja az összes eseménytípus naplózásához, vagy ha azt szeretné, hogy a program ne ellenőrizze az események naplózását.</span><span class="sxs-lookup"><span data-stu-id="45d33-143">You can specify All to audit all of the event types or None to specify that no events will be audited.</span></span>
<span data-ttu-id="45d33-144">Ha egyszerre adja meg az összes vagy a nincs beállítást, a parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="45d33-144">If you specify All or None at the same time, the cmdlet does not run.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: PlainSQL_Success, PlainSQL_Failure, ParameterizedSQL_Success, ParameterizedSQL_Failure, StoredProcedure_Success, StoredProcedure_Failure, Login_Success, Login_Failure, TransactionManagement_Success, TransactionManagement_Failure, All, None

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45d33-145">-PassThru</span><span class="sxs-lookup"><span data-stu-id="45d33-145">-PassThru</span></span>
<span data-ttu-id="45d33-146">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="45d33-146">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="45d33-147">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="45d33-147">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="45d33-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45d33-148">-ResourceGroupName</span></span>
<span data-ttu-id="45d33-149">Annak az erőforráscsoport a neve, amelyhez az adatbázis hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="45d33-149">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="45d33-150">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="45d33-150">-RetentionInDays</span></span>
<span data-ttu-id="45d33-151">A naplókban szereplő retenciós napok számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="45d33-151">Specifies the number of retention days for the audit logs table.</span></span>
<span data-ttu-id="45d33-152">A nulla (0) érték azt jelzi, hogy a táblázat nem marad meg.</span><span class="sxs-lookup"><span data-stu-id="45d33-152">A value of zero (0) means that the table is not retained.</span></span>
<span data-ttu-id="45d33-153">Az alapértelmezett érték a nulla.</span><span class="sxs-lookup"><span data-stu-id="45d33-153">The default value is zero.</span></span>
<span data-ttu-id="45d33-154">Ha nullánál nagyobb értéket ad meg, a *TableIdentifer* paraméter értékét kell megadnia.</span><span class="sxs-lookup"><span data-stu-id="45d33-154">If you specify a value greater than zero, you must specify a value for the *TableIdentifer* parameter.</span></span>

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

### <span data-ttu-id="45d33-155">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="45d33-155">-ServerName</span></span>
<span data-ttu-id="45d33-156">Az adatbázist tároló kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="45d33-156">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="45d33-157">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="45d33-157">-StorageAccountName</span></span>
<span data-ttu-id="45d33-158">Az adatbázis naplózásához használt tárolási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="45d33-158">Specifies the name of the storage account for auditing the database.</span></span>
<span data-ttu-id="45d33-159">A helyettesítő karakterek nem engedélyezettek.</span><span class="sxs-lookup"><span data-stu-id="45d33-159">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="45d33-160">Ehhez a paraméterhez nincs szükség.</span><span class="sxs-lookup"><span data-stu-id="45d33-160">This parameter is not required.</span></span>
<span data-ttu-id="45d33-161">Ha nem adja meg ezt a paramétert, a parancsmag az adatbázis naplózási házirendjének részeként megadott tárolási fiókot használja.</span><span class="sxs-lookup"><span data-stu-id="45d33-161">If you do not specify this parameter, the cmdlet uses the storage account that was defined previously as part of the auditing policy of the database.</span></span>
<span data-ttu-id="45d33-162">Ha most először adja meg az adatbázis-naplózási házirendet, és nem adja meg ezt a paramétert, a parancsmag nem működik.</span><span class="sxs-lookup"><span data-stu-id="45d33-162">If this is the first time a database auditing policy is defined and you do not specify this parameter, the cmdlet fails.</span></span>

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

### <span data-ttu-id="45d33-163">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="45d33-163">-StorageKeyType</span></span>
<span data-ttu-id="45d33-164">Itt adhatja meg, hogy a tárterület-hozzáférési kulcsok közül melyik használható.</span><span class="sxs-lookup"><span data-stu-id="45d33-164">Specifies which of the storage access keys to use.</span></span>
<span data-ttu-id="45d33-165">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="45d33-165">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="45d33-166">Elsődleges</span><span class="sxs-lookup"><span data-stu-id="45d33-166">Primary</span></span>
- <span data-ttu-id="45d33-167">Másodlagos: az alapértelmezett érték az elsődleges.</span><span class="sxs-lookup"><span data-stu-id="45d33-167">Secondary The default value is Primary.</span></span>

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

### <span data-ttu-id="45d33-168">-TableIdentifier</span><span class="sxs-lookup"><span data-stu-id="45d33-168">-TableIdentifier</span></span>
<span data-ttu-id="45d33-169">A naplókat tartalmazó tábla nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="45d33-169">Specifies the name of the audit logs table.</span></span>
<span data-ttu-id="45d33-170">Adja meg ezt az értéket, ha a *RetentionInDays* paraméterhez nullánál nagyobb értéket ad meg.</span><span class="sxs-lookup"><span data-stu-id="45d33-170">Specify this value if you specify a value greater than zero for the *RetentionInDays* parameter.</span></span>

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

### <span data-ttu-id="45d33-171">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="45d33-171">-Confirm</span></span>
<span data-ttu-id="45d33-172">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="45d33-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45d33-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45d33-173">-WhatIf</span></span>
<span data-ttu-id="45d33-174">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="45d33-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45d33-175">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="45d33-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45d33-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45d33-176">CommonParameters</span></span>
<span data-ttu-id="45d33-177">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="45d33-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45d33-178">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45d33-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45d33-179">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="45d33-179">INPUTS</span></span>

### <span data-ttu-id="45d33-180">Microsoft. Azure. Command. SQL. könyvvizsgálat. Model. AuditType</span><span class="sxs-lookup"><span data-stu-id="45d33-180">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditType</span></span>

### <span data-ttu-id="45d33-181">Microsoft. Azure. Command. SQL. könyvvizsgálat. Model. AuditActionGroups []</span><span class="sxs-lookup"><span data-stu-id="45d33-181">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span></span>

### <span data-ttu-id="45d33-182">System. string []</span><span class="sxs-lookup"><span data-stu-id="45d33-182">System.String[]</span></span>

### <span data-ttu-id="45d33-183">System. String</span><span class="sxs-lookup"><span data-stu-id="45d33-183">System.String</span></span>

### <span data-ttu-id="45d33-184">System. null ' 1 [[System. UInt32, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="45d33-184">System.Nullable\`1[[System.UInt32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="45d33-185">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="45d33-185">OUTPUTS</span></span>

### <span data-ttu-id="45d33-186">Microsoft. Azure. Command. SQL. könyvvizsgálat. Model. AuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="45d33-186">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditingPolicyModel</span></span>

## <span data-ttu-id="45d33-187">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="45d33-187">NOTES</span></span>

## <span data-ttu-id="45d33-188">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="45d33-188">RELATED LINKS</span></span>

[<span data-ttu-id="45d33-189">Get-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="45d33-189">Get-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Get-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="45d33-190">Remove-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="45d33-190">Remove-AzureRmSqlDatabaseAuditing</span></span>](./Remove-AzureRmSqlDatabaseAuditing.md)

[<span data-ttu-id="45d33-191">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="45d33-191">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


