---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/New-AzureRmDataMigrationSelectedDBObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationSelectedDBObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationSelectedDBObject.md
ms.openlocfilehash: d8303dadef33944addf63323e57727ef85acce6a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672110"
---
# New-AzureRmDataMigrationSelectedDBObject

## Áttekintés
Létrehoz egy adatbázis-beviteli objektumot, amely információt tartalmaz az áttelepítéshez szükséges forrás-és céladatbázis-adatbázisról.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### MigrateSqlServerSqlDb (alapértelmezett)
```
New-AzureRmDataMigrationSelectedDBObject -SourceDatabaseName <String> -TargetDatabaseName <String>
 [-MigrateSqlServerSqlDb] [-MakeSourceDbReadOnly]
 [-TableMap <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### MigrateSqlServerSqlDbMi
```
New-AzureRmDataMigrationSelectedDBObject -SourceDatabaseName <String> -TargetDatabaseName <String>
 [-MigrateSqlServerSqlDbMi] [-BackupFileShare <FileShare>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
Az New-AzureRmDataMigrationSelectedDB parancsmag létrehoz egy adatbázis-információt tartalmazó objektumot, amely információkat tartalmaz a forrás-és a céladatbázis, valamint a tábla megfeleltetéséről az áttelepítéshez. Ezt a parancsmagot a New-AzureRmDataMigrationTask parancsmag paraméterként használhatja.

## Példák

### Példa 1
```
PS C:\> New-AzureRmDataMigrationSelectedDB -MigrateSqlServerSqlDb -Name "HR" -TargetDatabaseName "HR_PSTEST" -TableMap $tableMap

Name TargetDatabaseName MakeSourceDbReadOnly TableMap
---- ------------------ -------------------- --------
HR   HR_PSTEST                         False {[HR.COUNTRIES, HR.COUNTRIES]}
```


### 2. példa
```
PS C:\> New-AzureRmDataMigrationSelectedDB -MigrateSqlServerSqlDbMi -Name "HR" -TargetDatabaseName "HR_PSTEST" -BackupFileShare $backupFileShare

Name RestoreDatabaseName BackupFileShare
---- ------------------- ---------------
HR   HRTest              Microsoft.Azure.Management.DataMigration.Models.FileShare
```


## PARAMÉTEREK

### -BackupFileShare
A fájlmegosztás, ahová az adatbázis forrás-adatbázis-fájljait biztonsági másolatot kell készíteni.
Ezzel a beállítással felülbírálhatja az egyes adatbázisokban tárolt fájlmegosztás adatait.
A kiszolgáló teljesen minősített tartománynevét használja.

```yaml
Type: Microsoft.Azure.Management.DataMigration.Models.FileShare
Parameter Sets: MigrateSqlServerSqlDbMi
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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

### -MakeSourceDbReadOnly
Az adatbázis írásvédett állapotba beállítása az áttelepítés előtt

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MigrateSqlServerSqlDb
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MigrateSqlServerSqlDb
Áttelepítési típus beállítása SQL Server-adatbázisba az SQL DB-áttelepítéshez.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MigrateSqlServerSqlDb
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MigrateSqlServerSqlDbMi
Áttelepítési típus beállítása SQL Server-re SQL DB MI áttelepítéssel.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MigrateSqlServerSqlDbMi
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceDatabaseName
A forrás-adatbázis neve.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TableMap
a forrás hozzárendelése a cél táblákhoz

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: MigrateSqlServerSqlDb
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetDatabaseName
A cél-adatbázis neve.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Microsoft. Azure. Management. DataMigration. models. fájlmegosztásról

## KIMENETEK

### Microsoft. Azure. Management. DataMigration. models. MigrateSqlServerSqlDbDatabaseInput

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
