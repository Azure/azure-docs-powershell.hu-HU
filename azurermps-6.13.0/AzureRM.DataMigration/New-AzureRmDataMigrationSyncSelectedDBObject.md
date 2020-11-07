---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/New-AzureRmDataMigrationSyncSelectedDBObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationSyncSelectedDBObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationSyncSelectedDBObject.md
ms.openlocfilehash: fc400c9eeb64acfa081d5a60a5e65089f415817b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679849"
---
# New-AzureRmDataMigrationSyncSelectedDBObject

## Áttekintés
Adatbázis-információ objektum létrehozása az áttelepítési feladathoz használt szinkronizálási forgatókönyvhez

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
New-AzureRmDataMigrationSyncSelectedDBObject -TargetDatabaseName <String> -SchemaName <String>
 -TableMap <Hashtable> [-MigrationSetting <Hashtable>] [-SourceSetting <Hashtable>]
 [-TargetSetting <Hashtable>] -SourceDatabaseName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás

Az New-AzureRmDataMigrationSyncSelectedDB parancsmag egy adatbázis-információ objektumra hivatkozik, amely a forrás-és a célként megadott adatbázisokkal kapcsolatos információkat tartalmazza.

## Példák

### Példa 1
```
PS C:\> $tableMap = New-Object 'system.collections.hashtable'
    $tableMap.Add("dbo.TestTable1", "dbo.TestTable1")
    $tableMap.Add("dbo.TestTable2","dbo.TestTable2")

    $selectedDbs = New-AzureRmDmsSyncSelectedDBObject 
        -TargetDatabaseName DatabaseName `
        -SchemaName dbo `
        -TableMap $tableMap `
        -SourceDatabaseName DatabaseName
```

Ez a példa létrehoz egy adatbázis metaadat-objektumot, amely leírja az $DatabaseName áttelepítési beállításait az adatbázis $DatabaseName.  

## PARAMÉTEREK

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

### -MigrationSetting
Az áttelepítési viselkedést beállító áttelepítési beállítások

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SchemaName
Áttelepítendő séma neve

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

### -SourceDatabaseName
A forrás-adatbázis neve.

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

### -SourceSetting
Forrás beállításai a forrás-végpont áttelepítési viselkedésének finomhangolásához

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TableMap
A forrás hozzárendelése a cél táblákhoz

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetDatabaseName
A céladatbázis neve

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

### -TargetSetting
Cél beállításai a végpont áttelepítési viselkedésének finomhangolásához

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs

## KIMENETEK

### Microsoft. Azure. Management. DataMigration. models. MigrateSqlServerSqlDbSyncTaskInput

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
