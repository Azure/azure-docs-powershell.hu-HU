---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 256AA6F4-D856-4713-A0AC-0DA1A145AA5C
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabasegeobackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackup.md
ms.openlocfilehash: 5ba899cba4c45c3d13858d8e274b333d613106dd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922658"
---
# Get-AzSqlDatabaseGeoBackup

## SYNOPSIS
Geodundáns biztonsági másolatot készít egy adatbázisról.

## SZINTAXIS

```
Get-AzSqlDatabaseGeoBackup [-ServerName] <String> [[-DatabaseName] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## LEÍRÁS
A **Get-AzSqlDatabaseGeoBackup** parancsmag meghatározott georedundáns biztonsági másolatot kap egy SQL-adatbázisról vagy az összes rendelkezésre álló geodundáns biztonsági másolatról egy adott kiszolgálón.
A georedundáns biztonsági másolat egy különálló földrajzi helyről származó adatfájlokat használó visszaállítható erőforrás.
A Geo-Restore segítségével visszaállíthatja a georedundáns biztonsági másolatot, ha egy regionális kimaradás miatt az adatbázist visszaállítja egy új régióba.
Ezt a parancsmagot az Azure SQL Server Stretch Database szolgáltatása is támogatja.

## PÉLDÁK

### 1. példa: Az összes georedundáns biztonsági másolat lekérte egy kiszolgálón
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

Ez a parancs minden geodundáns biztonsági másolatot kap egy adott kiszolgálón.

### 2. példa: Meghatározott georedundáns biztonsági másolat készítése
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

Ez a parancs a ContosoDatabase nevű geodundáns biztonsági másolatot kapja az adatbázisról.

### 3. példa: Az összes georedundáns biztonsági másolat lekérte egy kiszolgálón szűréssel
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "Contoso*"
```

Ez a parancs minden földrajzi redundáns biztonsági másolatot kap egy adott kiszolgálóról, amely a "Contoso" kezdetű.

## PARAMETERS

### -DatabaseName
A lekért adatbázis neve.

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
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés

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
Annak az erőforráscsoportnak a nevét adja meg, amelyhez az SQL-adatbázis-kiszolgáló hozzá van rendelve.

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

### -ServerName
Annak a kiszolgálónak a neve, amely a visszaállítható biztonsági másolatot adja meg.

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

### -Confirm
A parancsmag futtatása előtt a rendszer megerősítést kér.

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
A parancsmag futtatásakor a program megjeleníti, hogy mi történik.
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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

## KIMENETEK

### Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupModel

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Áttekintés: Felhőbeli üzletfolytonosság és adatbázis-katasztrófa-helyreállítás az SQL-adatbázissal](http://go.microsoft.com/fwlink/?LinkId=746881)

[Azure SQL-adatbázis helyreállítása kimaradásból](http://go.microsoft.com/fwlink/?LinkId=746882)

[Restore-AzSqlDatabase](./Restore-AzSqlDatabase.md)

[SQL-adatbázis dokumentációja](https://docs.microsoft.com/azure/sql-database/)
