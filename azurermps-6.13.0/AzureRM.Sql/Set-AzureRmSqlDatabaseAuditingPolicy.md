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
# Set-AzureRmSqlDatabaseAuditingPolicy

## Áttekintés
Az adatbázis naplózási házirendjének beállítása.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Set-AzureRmSqlDatabaseAuditingPolicy [-AuditType <AuditType>] [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-EventType <String[]>]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-TableIdentifier <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
A **set-AzureRmSqlDatabaseAuditingPolicy** parancsmag egy Azure SQL-adatbázis naplózási házirendjét módosítja.
A parancsmag használatához a *ResourceGroupName* , a *kiszolgálónév* és a *databasename* paraméterrel keresse meg az adatbázist.
Adja meg a *StorageAccountName* paramétert a naplók tárolási fiókjának a megadásához, illetve a *StorageKeyType* paramétert a tárolási kulcsok meghatározásához.
Azt is megadhatja, hogy az *RetentionInDays* és a *TableIdentifier* paramétereinek értéke megadásával meghatározza a naplózási naplók tábla adatmegőrzési listáját.
Adja meg a *EventType* paramétert annak meghatározásához, hogy milyen típusú események legyenek naplózva.
A parancsmag sikeres futtatása után az adatbázis naplózása engedélyezve van.
Ha a táblázat naplózása, ha az adatbázis a kiszolgálójának házirendjét használta a naplózás megkezdése előtt, a naplózás leállítja a házirend használatát. BLOB-naplózás esetén, ha az adatbázis a kiszolgálójának házirendjét használta naplózásra, mielőtt ezt a parancsmagot futtatta, a naplózási házirendek egymás mellett jelennek meg.
Ha a parancsmag sikerrel jár, és a *PassThru* paramétert használja, az adatbázis-azonosítók mellett az aktuális naplózási házirendet leíró objektumot ad eredményül.
Az adatbázis-azonosítók közé tartoznak a következők: a **ResourceGroupName** , a **kiszolgálónév** és a **databasename**.
Ezt a parancsmagot az SQL Server stretch Database szolgáltatása is támogatja az Azure-ban.

## Példák

### Példa 1: az adatbázis naplózási házirendjének beállítása táblázat-naplózás használatára
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -AuditType Table -StorageAccountName "Storage31"
```

Ez a parancs a Server01 nevű Database01 nevű adatbázis naplózási házirendjét a Storage31 nevű tárolási fiók használatára állítja be.

### 2. példa: az adatbázis meglévő naplózási házirendjének a Storage Account (tárterület) kulcsának beállítása
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -StorageAccountKey Secondary
```

Ez a parancs a Server01 található Database01 nevű adatbázis naplózási házirendjét úgy állítja be, hogy ugyanazt a tárolási fióknevet használja, de most már használja a másodlagos kulcsot.

### 3. példa: egy adatbázis naplózási házirendjének beállítása adott eseménytípus használatához
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -EventType Login_Failure
```

### Példa 4: az adatbázis naplózási házirendjének beállítása blob-naplózás használatára
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -AuditType Blob -StorageAccountName "Storage31" -AuditActionGroup "SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP", "FAILED_DATABASE_AUTHENTICATION_GROUP" -AuditAction "UPDATE ON database::[Database01] BY [public]"  -RetentionInDays 8
```

Ez a parancs a Server01 található Database01 nevű adatbázis naplózási házirendjét állítja be.
A házirend naplózza a Login_Failure eseménytípus típusát.
A parancs nem módosítja a tárolási beállításokat.

## PARAMÉTEREK

### -AuditAction
Adjon meg egy vagy több naplózási műveletet.
Ez a paraméter csak a blob-naplózásra érvényes.

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

### -AuditActionGroup
Adjon meg egy vagy több naplózási műveleti csoportot.
Ez a paraméter csak a blob-naplózásra érvényes.

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

### -AuditType
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

### -DatabaseName
Az adatbázis nevét adja meg.

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

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés

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

### -EventType
A naplózni kívánt esemény típusait adja meg.
Ez a paraméter csak a tábla naplózására érvényes.
Több eseménytípus is megadható.
A mind lehetőséget megadhatja az összes eseménytípus naplózásához, vagy ha azt szeretné, hogy a program ne ellenőrizze az események naplózását.
Ha egyszerre adja meg az összes vagy a nincs beállítást, a parancsmag nem fut.

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

### -PassThru
Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.
Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.

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

### -ResourceGroupName
Annak az erőforráscsoport a neve, amelyhez az adatbázis hozzá van rendelve.

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

### -RetentionInDays
A naplókban szereplő retenciós napok számát adja meg.
A nulla (0) érték azt jelzi, hogy a táblázat nem marad meg.
Az alapértelmezett érték a nulla.
Ha nullánál nagyobb értéket ad meg, a *TableIdentifer* paraméter értékét kell megadnia.

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

### -Kiszolgálónév
Az adatbázist tároló kiszolgáló nevét adja meg.

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

### -StorageAccountName
Az adatbázis naplózásához használt tárolási fiók nevét adja meg.
A helyettesítő karakterek nem engedélyezettek.
Ehhez a paraméterhez nincs szükség.
Ha nem adja meg ezt a paramétert, a parancsmag az adatbázis naplózási házirendjének részeként megadott tárolási fiókot használja.
Ha most először adja meg az adatbázis-naplózási házirendet, és nem adja meg ezt a paramétert, a parancsmag nem működik.

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

### -StorageKeyType
Itt adhatja meg, hogy a tárterület-hozzáférési kulcsok közül melyik használható.
A paraméter elfogadható értékei a következők:
- Elsődleges
- Másodlagos: az alapértelmezett érték az elsődleges.

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

### -TableIdentifier
A naplókat tartalmazó tábla nevét adja meg.
Adja meg ezt az értéket, ha a *RetentionInDays* paraméterhez nullánál nagyobb értéket ad meg.

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

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

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

### -WhatIf
Annak megjelenítése, hogy mi történik, ha a parancsmag fut.
A parancsmag nem fut.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Microsoft. Azure. Command. SQL. könyvvizsgálat. Model. AuditType

### Microsoft. Azure. Command. SQL. könyvvizsgálat. Model. AuditActionGroups []

### System. string []

### System. String

### System. null ' 1 [[System. UInt32, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]

## KIMENETEK

### Microsoft. Azure. Command. SQL. könyvvizsgálat. Model. AuditingPolicyModel

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmSqlDatabaseAuditingPolicy](./Get-AzureRmSqlDatabaseAuditingPolicy.md)

[Remove-AzureRmSqlDatabaseAuditing](./Remove-AzureRmSqlDatabaseAuditing.md)

[SQL-adatbázis dokumentációja](https://docs.microsoft.com/azure/sql-database/)


