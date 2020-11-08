---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 256AA6F4-D856-4713-A0AC-0DA1A145AA5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasegeobackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackup.md
ms.openlocfilehash: 0ca3a6c467ab5fd7dd681164d88686a6360394ee
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195312"
---
# Get-AzSqlDatabaseGeoBackup

## Áttekintés
Egy adatbázis geo-redundáns biztonsági másolatát kapja.

## SZINTAXISA

```
Get-AzSqlDatabaseGeoBackup [-ServerName] <String> [[-DatabaseName] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
A **Get-AzSqlDatabaseGeoBackup** PARANCSMAG egy SQL-adatbázis meghatározott geo-redundáns biztonsági másolatát kapja, vagy az összes rendelkezésre álló geo-redundáns biztonsági mentést egy adott kiszolgálón.
A Geo-redundáns biztonsági másolat egy helyreállítható erőforrás, amely külön földrajzi helyről származó adatfájlokat használ.
A Geo-Restore segítségével visszaállíthatja a Geo-redundáns biztonsági másolatot az adatbázis új területre való visszaállításához regionális leállás esetén.
Ezt a parancsmagot az SQL Server stretch Database szolgáltatása is támogatja az Azure-ban.

## Példák

### Példa 1: minden geo-redundáns biztonsági másolat beolvasása a kiszolgálón
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

Ez a parancs a megadott kiszolgálón elérhető geo-redundáns biztonsági másolatokat kapja meg.

### 2. példa: meghatározott geo-redundáns biztonsági másolat beszerzése
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

Ez a parancs a ContosoDatabase nevű adatbázis geo-redundáns biztonsági másolatát kapja.

### 3. példa: minden geo-redundáns biztonsági másolat beolvasása a kiszolgálón szűréssel
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "Contoso*"
```

Ez a parancs minden elérhető geo-redundáns biztonsági mentést kap egy olyan kiszolgálón, amely "contoso" kezdetű.

## PARAMÉTEREK

### -DatabaseName
A beolvasott adatbázis nevét adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés

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

### -ResourceGroupName
Annak az erőforrás-csoportnak a nevét adja meg, amelyhez az SQL-adatbázis kiszolgálója van rendelve.

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

### -Kiszolgálónév
Itt adhatja meg annak a kiszolgálónak a nevét, amely a visszaállítani kívánt biztonsági másolatot tárolja.

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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.

## BEMENETEK

### System. String

## KIMENETEK

### Microsoft. Azure. Command. SQL. backup. Model. AzureSqlDatabaseGeoBackupModel

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Áttekintés: a Felhőbeli üzletmenet folytonossága és az adatbázis katasztrófa-elhárítása SQL-adatbázissal](http://go.microsoft.com/fwlink/?LinkId=746881)

[Azure SQL-adatbázis helyreállítása leállás esetén](http://go.microsoft.com/fwlink/?LinkId=746882)

[Restore-AzSqlDatabase](./Restore-AzSqlDatabase.md)

[SQL-adatbázis dokumentációja](https://docs.microsoft.com/azure/sql-database/)
