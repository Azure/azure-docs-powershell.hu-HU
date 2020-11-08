---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: CB601E21-424D-4B09-85E5-A4B2A5068267
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2b7674cb5b7abc489dc6aa6d3746f499b9686312
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016403"
---
# Stop-AzureSqlDatabaseCopy

## Áttekintés
Folytonos másolási kapcsolat megszüntetése

## SZINTAXISA

### ByInputObject
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -DatabaseCopy <DatabaseCopy> [-ForcedTermination] [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByDatabase
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-ForcedTermination] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByDatabaseName
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-ForcedTermination] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Leírás
A **stop-AzureSqlDatabaseCopy** parancsmag folytonos másolási kapcsolatot szüntet meg.
Ez a parancsmag leállítja a forrásadatbázis és a másodlagos vagy a cél adatbázis közötti adatmozgást, majd a másodlagos adatbázis állapotát különálló online adatbázisként módosítja.

A folyamatos másolási viszonyok, a megszüntetési vagy a tervezett megszűnések, valamint a kényszer megszűnése két módon végezhető el a lehetséges adatvesztéssel.
A forrás adatbázist tároló kiszolgálón futtathatja ezt a parancsmagot a megszüntetés vagy a kényszeres lemondási mód használatával.
A másodlagos adatbázist tároló kiszolgálón kényszerített befejezési módot kell használnia.

A tervezett megszüntetés csak akkor várja a másodlagos adatbázisba, ha a forrástartományban futtatott összes tranzakciót futtatta a forrás adatbázisból.
A kényszeres megszűnés nem várja meg az esetleges függőben lévő lekötött tranzakciók replikálását, és a másodlagos adatbázis esetleges adatvesztését is okozhatja.

Amíg a replikációs állapot FÜGGŐben van, csak a kényszer megszűnése lehet sikeres a folyamatos másolási kapcsolat befejezése.
Ha a replikációs állapot FÜGGŐben van, a záró érték nem használható.

## Példák

### 1. példa: folyamatos másolati kapcsolat megszüntetése
```
PS C:\>Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

Ez a parancs a lpqd0zbr8y nevű kiszolgálón a rendelések nevű adatbázis folyamatos másolati kapcsolatát zárja le.
A bk0b8kf658 nevű kiszolgáló a másodlagos adatbázist tárolja.

### 2. példa: folyamatos másolati kapcsolat megszüntetése
```
PS C:\>$DatabaseCopy = Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders"
PS C:\> $DatabaseCopy | Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -ForcedTermination
```

Az első parancs a lpqd0zbr8y nevű kiszolgálón a rendelések nevű adatbázis adatbázis-másolási kapcsolatát kapja.

A második parancs a másodlagos adatbázist tároló kiszolgálóról folyamatosan megszünteti a folyamatos másolási viszonyt.

## PARAMÉTEREK

### -Database (adatbázis)
Egy olyan objektumot ad meg, amely a Source Azure SQL-adatbázist jelöli.
Ez a parancsmag lezárja az adatbázis folytonos másolati kapcsolatát, amelyet a paraméter határoz meg.

```yaml
Type: Database
Parameter Sets: ByDatabase
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseCopy
Egy adatbázist jelképező objektumot ad meg.
Ez a parancsmag lezárja az adatbázis folytonos másolati kapcsolatát, amelyet a paraméter határoz meg.
Ez a paraméter elfogadja a csővezeték-bevitelt.

```yaml
Type: DatabaseCopy
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseName
Az adatbázis nevét adja meg.
Ez a parancsmag lezárja az adatbázis folytonos másolati kapcsolatát, amelyet a paraméter határoz meg.

```yaml
Type: String
Parameter Sets: ByDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.

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

### -ForcedTermination
Jelzi, hogy ez a parancsmag a folyamatos másolási viszony kényszeres megszüntetését okozta.
A kényszeres megszűnés az adatvesztéssel járhat.
Ha a parancsmagot egy olyan kiszolgálón szeretné futtatni, amelyen a céladatbázis található, ezt a paramétert kell megadnia.
Ha a parancsmagot a forrás adatbázist tároló kiszolgálón szeretné futtatni, ha a másodlagos adatbázis nem érhető el, akkor ezt a paramétert kell megadnia.

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

### -PartnerDatabase
A másodlagos adatbázis nevét adja meg.
Ha megad egy nevet, a forrás-adatbázis nevének egyeznie kell.

```yaml
Type: String
Parameter Sets: ByDatabase, ByDatabaseName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartnerServer
A célként megadott adatbázist tároló kiszolgáló neve.

```yaml
Type: String
Parameter Sets: ByDatabase, ByDatabaseName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.
Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Kiszolgálónév
Annak a kiszolgálónak a nevét adja meg, amelyen a forrás adatbázis található.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

```yaml
Type: SwitchParameter
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
Type: SwitchParameter
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

### Microsoft. WindowsAzure. Command. SqlDatabase. Model. DatabaseCopy

### Microsoft. WindowsAzure. Command. SqlDatabase. Services. Server. Database

## KIMENETEK

### Nincs

## MEGJEGYZI
* Hitelesítés: Ez a parancsmag tanúsítvány-alapú hitelesítést követel meg. Példa arra, hogy hogyan állíthatja be a jelenlegi előfizetést a tanúsítványalapú hitelesítéssel, ha a **New-AzureSqlDatabaseServerContext** parancsmagot használja.
* Korlátozások: a másodlagos adatbázist tároló kiszolgálón csak a kényszeres megszüntetés támogatott.
* A megszüntetés hatása a volt másodlagos adatbázisra: a megszüntetést követően a másodlagos adatbázis független adatbázis lesz. Ha a másodlagos adatbázison már elkészült a kivetés, az adatbázis befejezését követően teljes hozzáférésre nyitva kell lennie. Ha a forrásadatbázis egy írható-olvasható adatbázis, a volt másodlagos adatbázis is írható-olvasható adatbázis lesz.

  Ha a kivetés jelenleg folyamatban van, a vetés megszakad, és a volt másodlagos adatbázis nem lesz látható a másodlagos adatbázist tároló kiszolgálón.

* A forrásadatok csak olvasható módra állíthatók be. Ez biztosítja, hogy a forrás-és másodlagos adatbázisokat a befejezés után szinkronizálja a program, és gondoskodjon arról, hogy a lemondáskor ne történjen semmilyen tranzakció véglegesítése. A Befejezés befejezése után állítsa vissza a forrást olvasási és írási módra. A korábbi másodlagos adatbázist tetszés szerint is megadhatja olvasási és írási módra.
* Monitoring: Ha ellenőrizni szeretné a műveletek állapotát a folyamatos másolási kapcsolat forrásában és céljában, használja a **Get-AzureSqlDatabaseOperation** parancsmagot.

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Azure SQL-adatbázis](https://azure.microsoft.com/en-us/services/sql-database/)

[Azure SQL-adatbázisok műveletei](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Adatbázis-példány leállítása](https://msdn.microsoft.com/en-us/library/dn509573.aspx)

[Azure SQL-adatbázis-parancsmagok](./Azure.SQLDatabase.md)

[Get-AzureSqlDatabaseCopy](./Get-AzureSqlDatabaseCopy.md)

[Start-AzureSqlDatabaseCopy](./Start-AzureSqlDatabaseCopy.md)


