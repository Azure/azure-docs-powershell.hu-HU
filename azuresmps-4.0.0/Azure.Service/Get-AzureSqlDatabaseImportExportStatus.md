---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 4661C479-6E3B-425D-B9D2-B36D7A83130C
online version: ''
schema: 2.0.0
ms.openlocfilehash: c3c55ebd22337a8078f3ae495b3901317f4201e0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016294"
---
# Get-AzureSqlDatabaseImportExportStatus

## Áttekintés
Az importálási vagy exportálási kérés állapotát kapja meg.

## SZINTAXISA

### ByConnectionInfo
```
Get-AzureSqlDatabaseImportExportStatus -Username <String> -Password <String> -ServerName <String>
 -RequestId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByRequestObject
```
Get-AzureSqlDatabaseImportExportStatus -Request <ImportExportRequest> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Leírás
A **Get-AzureSqlDatabaseImportExportStatus** parancsmag az importálási vagy exportálási kérés állapotát kapja meg.
A Start-AzureSqlDatabaseImport vagy Start-AzureSqlDatabaseExport parancsmag kezdeményezi a kéréseket.
Megadhatja a Request objektumot a *Request* paraméterrel, vagy a *kérelemazonosító* paraméterrel, illetve a *Felhasználónév* , a *jelszó* és a *kiszolgálónév* paraméter használatával is megadhatja a kérést.

## Példák

### Példa 1: exportálási kérés állapotának beszerzése
```
PS C:\> $ExportRequest = Start-AzureSqlDatabaseExport -SqlConnectionContext $SqlContext -StorageContainer $Container -DatabaseName $DatabaseName -BlobName $BlobName
PS C:\> Get-AzureSqlDatabaseImportExportStatus -Request $ExportRequest
```

Az első parancs létrehoz egy exportálási kérést, majd a $ExportRequest változóban tárolja.

A második parancs a $ExportRequestban tárolt exportálási kérés állapotát kapja meg.

## PARAMÉTEREK

### -Jelszó
Az Azure SQL adatbázis-kiszolgálóhoz való csatlakozáshoz szükséges jelszót adja meg.
Ezt a paramétert akkor kell megadnia, ha a *kérelemazonosító* paramétert adja meg.

```yaml
Type: String
Parameter Sets: ByConnectionInfo
Aliases: 

Required: True
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

### -Request (kérés)
Egy **ImportExportRequest** objektumot ad meg.
Importálási vagy exportálási kérési objektum beolvasásához használja a Start-AzureSqlDatabaseImport vagy Start-AzureSqlDatabaseExport parancsmagot.

```yaml
Type: ImportExportRequest
Parameter Sets: ByRequestObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Kérelemazonosító
Annak az importálási vagy exportálási műveletnek az GUID-azonosítóját adja meg, amelyre a parancsmag állapota bekerül.
Ha ezt a paramétert adja meg, meg kell adnia a *Felhasználónév* , a *jelszó* és a *kiszolgálónév* paramétert.

```yaml
Type: String
Parameter Sets: ByConnectionInfo
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Kiszolgálónév
Az Azure SQL adatbázis-kiszolgáló nevét adja meg.
Ezt a paramétert akkor kell megadnia, ha a *kérelemazonosító* paramétert adja meg.

```yaml
Type: String
Parameter Sets: ByConnectionInfo
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Felhasználónév
Annak a felhasználónak a nevét adja meg, amely az Azure SQL adatbázis-kiszolgálóhoz való csatlakozáshoz szükséges.
Ezt a paramétert akkor kell megadnia, ha a *kérelemazonosító* paramétert adja meg.

```yaml
Type: String
Parameter Sets: ByConnectionInfo
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

## KIMENETEK

### Microsoft. WindowsAzure. Command. SqlDatabase. Services. ImportExport. StatusInfo

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Azure SQL-adatbázis](https://azure.microsoft.com/en-us/services/sql-database/)

[Importálás exportálása adatbázis-állapot](https://msdn.microsoft.com/en-us/library/azure/dn781289.aspx)

[Azure SQL-adatbázisok műveletei](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Start-AzureSqlDatabaseExport](./Start-AzureSqlDatabaseExport.md)

[Start-AzureSqlDatabaseImport](./Start-AzureSqlDatabaseImport.md)


