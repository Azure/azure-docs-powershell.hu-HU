---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditingPolicy.md
ms.openlocfilehash: 99fb9bf57f056a869310de2fe27d00a72ce5d8c3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493316"
---
# <span data-ttu-id="d25a3-101">Set-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="d25a3-101">Set-AzureRmSqlDatabaseAuditingPolicy</span></span>

## <span data-ttu-id="d25a3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d25a3-102">SYNOPSIS</span></span>
<span data-ttu-id="d25a3-103">Az adatbázis naplózási házirendjének beállítása.</span><span class="sxs-lookup"><span data-stu-id="d25a3-103">Sets the auditing policy for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d25a3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d25a3-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseAuditingPolicy [-AuditType <AuditType>] [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-EventType <String[]>]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-TableIdentifier <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d25a3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d25a3-105">DESCRIPTION</span></span>
<span data-ttu-id="d25a3-106">A **set-AzureRmSqlDatabaseAuditingPolicy** parancsmag egy Azure SQL-adatbázis naplózási házirendjét módosítja.</span><span class="sxs-lookup"><span data-stu-id="d25a3-106">The **Set-AzureRmSqlDatabaseAuditingPolicy** cmdlet changes the auditing policy of an Azure SQL database.</span></span>
<span data-ttu-id="d25a3-107">A parancsmag használatához a *ResourceGroupName* , a *kiszolgálónév* és a *databasename* paraméterrel keresse meg az adatbázist.</span><span class="sxs-lookup"><span data-stu-id="d25a3-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="d25a3-108">Adja meg a *StorageAccountName* paramétert a naplók tárolási fiókjának a megadásához, illetve a *StorageKeyType* paramétert a tárolási kulcsok meghatározásához.</span><span class="sxs-lookup"><span data-stu-id="d25a3-108">Specify the *StorageAccountName* parameter to specify the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span>

<span data-ttu-id="d25a3-109">Azt is megadhatja, hogy az *RetentionInDays* és a *TableIdentifier* paramétereinek értéke megadásával meghatározza a naplózási naplók tábla adatmegőrzési listáját.</span><span class="sxs-lookup"><span data-stu-id="d25a3-109">You can also define retention for the audit logs table by setting the value of the *RetentionInDays* and *TableIdentifier* parameters to define the period and the seed for the audit log table names.</span></span>
<span data-ttu-id="d25a3-110">Adja meg a *EventType* paramétert annak meghatározásához, hogy milyen típusú események legyenek naplózva.</span><span class="sxs-lookup"><span data-stu-id="d25a3-110">Specify the *EventType* parameter to define which event types to audit.</span></span>

<span data-ttu-id="d25a3-111">A parancsmag sikeres futtatása után az adatbázis naplózása engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="d25a3-111">After the cmdlet runs successfully, auditing of the database is enabled.</span></span>
<span data-ttu-id="d25a3-112">Ha az adatbázis a kiszolgálója házirendjének naplózását használta a parancsmag futtatása előtt, a naplózás nem használja ezt a házirendet.</span><span class="sxs-lookup"><span data-stu-id="d25a3-112">If the database used the policy of its server for auditing before you ran this cmdlet, auditing stops using that policy.</span></span>
<span data-ttu-id="d25a3-113">Ha a parancsmag sikerrel jár, és a *PassThru* paramétert használja, az adatbázis-azonosítók mellett az aktuális naplózási házirendet leíró objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="d25a3-113">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current auditing policy in addition to the database identifiers.</span></span>
<span data-ttu-id="d25a3-114">Az adatbázis-azonosítók közé tartoznak a következők: a **ResourceGroupName** , a **kiszolgálónév** és a **databasename**.</span><span class="sxs-lookup"><span data-stu-id="d25a3-114">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>

<span data-ttu-id="d25a3-115">Ezt a parancsmagot az SQL Server stretch Database szolgáltatása is támogatja az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="d25a3-115">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="d25a3-116">Példák</span><span class="sxs-lookup"><span data-stu-id="d25a3-116">EXAMPLES</span></span>

### <span data-ttu-id="d25a3-117">Példa 1: az adatbázis naplózási házirendjének beállítása táblázat-naplózás használatára</span><span class="sxs-lookup"><span data-stu-id="d25a3-117">Example 1: Set the auditing policy of a database to use Table auditing</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -AuditType Table -StorageAccountName "Storage31"
```

<span data-ttu-id="d25a3-118">Ez a parancs a Server01 nevű Database01 nevű adatbázis naplózási házirendjét a Storage31 nevű tárolási fiók használatára állítja be.</span><span class="sxs-lookup"><span data-stu-id="d25a3-118">This command sets the auditing policy of database named Database01 located on Server01 to use the storage account named Storage31.</span></span>

### <span data-ttu-id="d25a3-119">2. példa: az adatbázis meglévő naplózási házirendjének a Storage Account (tárterület) kulcsának beállítása</span><span class="sxs-lookup"><span data-stu-id="d25a3-119">Example 2: Set the storage account key of an existing auditing policy of a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -StorageAccountKey Secondary
```

<span data-ttu-id="d25a3-120">Ez a parancs a Server01 található Database01 nevű adatbázis naplózási házirendjét úgy állítja be, hogy ugyanazt a tárolási fióknevet használja, de most már használja a másodlagos kulcsot.</span><span class="sxs-lookup"><span data-stu-id="d25a3-120">This command sets the auditing policy of database named Database01 located on Server01 to keep using the same storage account name but to now use the secondary key.</span></span>

### <span data-ttu-id="d25a3-121">3. példa: egy adatbázis naplózási házirendjének beállítása adott eseménytípus használatához</span><span class="sxs-lookup"><span data-stu-id="d25a3-121">Example 3: Set the auditing policy of a database to use a specific event type</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -EventType Login_Failure
```

### <span data-ttu-id="d25a3-122">Példa 4: az adatbázis naplózási házirendjének beállítása blob-naplózás használatára</span><span class="sxs-lookup"><span data-stu-id="d25a3-122">Example 4: Set the auditing policy of a database to use Blob auditing</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -AuditType Blob -StorageAccountName "Storage31" -AuditActionGroup "SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP", "FAILED_DATABASE_AUTHENTICATION_GROUP" -AuditAction "UPDATE ON database::[Database01] BY [public]"  -RetentionInDays 8
```

<span data-ttu-id="d25a3-123">Ez a parancs a Server01 található Database01 nevű adatbázis naplózási házirendjét állítja be.</span><span class="sxs-lookup"><span data-stu-id="d25a3-123">This command sets the auditing policy of database named Database01 located on Server01.</span></span>
<span data-ttu-id="d25a3-124">A házirend naplózza a Login_Failure eseménytípus típusát.</span><span class="sxs-lookup"><span data-stu-id="d25a3-124">The policy logs the Login_Failure event type.</span></span>
<span data-ttu-id="d25a3-125">A parancs nem módosítja a tárolási beállításokat.</span><span class="sxs-lookup"><span data-stu-id="d25a3-125">The command does not change the storage settings.</span></span>

## <span data-ttu-id="d25a3-126">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d25a3-126">PARAMETERS</span></span>

### <span data-ttu-id="d25a3-127">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="d25a3-127">-AuditAction</span></span>
<span data-ttu-id="d25a3-128">Adjon meg egy vagy több naplózási műveletet.</span><span class="sxs-lookup"><span data-stu-id="d25a3-128">Specify one or more audit actions.</span></span>
<span data-ttu-id="d25a3-129">Ez a paraméter csak a blob-naplózásra érvényes.</span><span class="sxs-lookup"><span data-stu-id="d25a3-129">This parameter is only applicable to Blob auditing.</span></span>

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

### <span data-ttu-id="d25a3-130">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="d25a3-130">-AuditActionGroup</span></span>
<span data-ttu-id="d25a3-131">Adjon meg egy vagy több naplózási műveleti csoportot.</span><span class="sxs-lookup"><span data-stu-id="d25a3-131">Specify one or more audit action groups.</span></span>
<span data-ttu-id="d25a3-132">Ez a paraméter csak a blob-naplózásra érvényes.</span><span class="sxs-lookup"><span data-stu-id="d25a3-132">This parameter is only applicable to Blob auditing.</span></span>

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

### <span data-ttu-id="d25a3-133">-AuditType</span><span class="sxs-lookup"><span data-stu-id="d25a3-133">-AuditType</span></span>
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

### <span data-ttu-id="d25a3-134">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d25a3-134">-DatabaseName</span></span>
<span data-ttu-id="d25a3-135">Az adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d25a3-135">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="d25a3-136">-EventType</span><span class="sxs-lookup"><span data-stu-id="d25a3-136">-EventType</span></span>
<span data-ttu-id="d25a3-137">A naplózni kívánt esemény típusait adja meg.</span><span class="sxs-lookup"><span data-stu-id="d25a3-137">Specifies the event types to audit.</span></span>
<span data-ttu-id="d25a3-138">Ez a paraméter csak a tábla naplózására érvényes.</span><span class="sxs-lookup"><span data-stu-id="d25a3-138">This parameter is only applicable to Table auditing.</span></span>

<span data-ttu-id="d25a3-139">Több eseménytípus is megadható.</span><span class="sxs-lookup"><span data-stu-id="d25a3-139">You can specify several event types.</span></span>
<span data-ttu-id="d25a3-140">A mind lehetőséget megadhatja az összes eseménytípus naplózásához, vagy ha azt szeretné, hogy a program ne ellenőrizze az események naplózását.</span><span class="sxs-lookup"><span data-stu-id="d25a3-140">You can specify All to audit all of the event types or None to specify that no events will be audited.</span></span>
<span data-ttu-id="d25a3-141">Ha egyszerre adja meg az összes vagy a nincs beállítást, a parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d25a3-141">If you specify All or None at the same time, the cmdlet does not run.</span></span>

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

### <span data-ttu-id="d25a3-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d25a3-142">-PassThru</span></span>
<span data-ttu-id="d25a3-143">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="d25a3-143">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d25a3-144">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="d25a3-144">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d25a3-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d25a3-145">-ResourceGroupName</span></span>
<span data-ttu-id="d25a3-146">Annak az erőforráscsoport a neve, amelyhez az adatbázis hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="d25a3-146">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="d25a3-147">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="d25a3-147">-RetentionInDays</span></span>
<span data-ttu-id="d25a3-148">A naplókban szereplő retenciós napok számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d25a3-148">Specifies the number of retention days for the audit logs table.</span></span>
<span data-ttu-id="d25a3-149">A nulla (0) érték azt jelzi, hogy a táblázat nem marad meg.</span><span class="sxs-lookup"><span data-stu-id="d25a3-149">A value of zero (0) means that the table is not retained.</span></span>
<span data-ttu-id="d25a3-150">Az alapértelmezett érték a nulla.</span><span class="sxs-lookup"><span data-stu-id="d25a3-150">The default value is zero.</span></span>
<span data-ttu-id="d25a3-151">Ha nullánál nagyobb értéket ad meg, a *TableIdentifer* paraméter értékét kell megadnia.</span><span class="sxs-lookup"><span data-stu-id="d25a3-151">If you specify a value greater than zero, you must specify a value for the *TableIdentifer* parameter.</span></span>

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

### <span data-ttu-id="d25a3-152">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="d25a3-152">-ServerName</span></span>
<span data-ttu-id="d25a3-153">Az adatbázist tároló kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d25a3-153">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="d25a3-154">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d25a3-154">-StorageAccountName</span></span>
<span data-ttu-id="d25a3-155">Az adatbázis naplózásához használt tárolási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d25a3-155">Specifies the name of the storage account for auditing the database.</span></span>
<span data-ttu-id="d25a3-156">A helyettesítő karakterek nem engedélyezettek.</span><span class="sxs-lookup"><span data-stu-id="d25a3-156">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="d25a3-157">Ehhez a paraméterhez nincs szükség.</span><span class="sxs-lookup"><span data-stu-id="d25a3-157">This parameter is not required.</span></span>
<span data-ttu-id="d25a3-158">Ha nem adja meg ezt a paramétert, a parancsmag az adatbázis naplózási házirendjének részeként megadott tárolási fiókot használja.</span><span class="sxs-lookup"><span data-stu-id="d25a3-158">If you do not specify this parameter, the cmdlet uses the storage account that was defined previously as part of the auditing policy of the database.</span></span>
<span data-ttu-id="d25a3-159">Ha most először adja meg az adatbázis-naplózási házirendet, és nem adja meg ezt a paramétert, a parancsmag nem működik.</span><span class="sxs-lookup"><span data-stu-id="d25a3-159">If this is the first time a database auditing policy is defined and you do not specify this parameter, the cmdlet fails.</span></span>

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

### <span data-ttu-id="d25a3-160">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="d25a3-160">-StorageKeyType</span></span>
<span data-ttu-id="d25a3-161">Itt adhatja meg, hogy a tárterület-hozzáférési kulcsok közül melyik használható.</span><span class="sxs-lookup"><span data-stu-id="d25a3-161">Specifies which of the storage access keys to use.</span></span>
<span data-ttu-id="d25a3-162">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="d25a3-162">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d25a3-163">Elsődleges</span><span class="sxs-lookup"><span data-stu-id="d25a3-163">Primary</span></span>
- <span data-ttu-id="d25a3-164">Másodlagos</span><span class="sxs-lookup"><span data-stu-id="d25a3-164">Secondary</span></span>

<span data-ttu-id="d25a3-165">Az alapértelmezett érték az elsődleges.</span><span class="sxs-lookup"><span data-stu-id="d25a3-165">The default value is Primary.</span></span>

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

### <span data-ttu-id="d25a3-166">-TableIdentifier</span><span class="sxs-lookup"><span data-stu-id="d25a3-166">-TableIdentifier</span></span>
<span data-ttu-id="d25a3-167">A naplókat tartalmazó tábla nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d25a3-167">Specifies the name of the audit logs table.</span></span>
<span data-ttu-id="d25a3-168">Adja meg ezt az értéket, ha a *RetentionInDays* paraméterhez nullánál nagyobb értéket ad meg.</span><span class="sxs-lookup"><span data-stu-id="d25a3-168">Specify this value if you specify a value greater than zero for the *RetentionInDays* parameter.</span></span>

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

### <span data-ttu-id="d25a3-169">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d25a3-169">-Confirm</span></span>
<span data-ttu-id="d25a3-170">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d25a3-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d25a3-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d25a3-171">-WhatIf</span></span>
<span data-ttu-id="d25a3-172">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d25a3-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d25a3-173">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d25a3-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d25a3-174">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d25a3-174">-DefaultProfile</span></span>
<span data-ttu-id="d25a3-175">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d25a3-175">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d25a3-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d25a3-176">CommonParameters</span></span>
<span data-ttu-id="d25a3-177">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d25a3-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d25a3-178">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d25a3-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d25a3-179">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d25a3-179">INPUTS</span></span>

## <span data-ttu-id="d25a3-180">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d25a3-180">OUTPUTS</span></span>

### <span data-ttu-id="d25a3-181">Microsoft. Azure. Command. SQL. Security. Model. DatabaseAuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="d25a3-181">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseAuditingPolicyModel</span></span>

## <span data-ttu-id="d25a3-182">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d25a3-182">NOTES</span></span>

## <span data-ttu-id="d25a3-183">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d25a3-183">RELATED LINKS</span></span>

[<span data-ttu-id="d25a3-184">Get-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="d25a3-184">Get-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Get-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="d25a3-185">Remove-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="d25a3-185">Remove-AzureRmSqlDatabaseAuditing</span></span>](./Remove-AzureRmSqlDatabaseAuditing.md)

[<span data-ttu-id="d25a3-186">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="d25a3-186">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


