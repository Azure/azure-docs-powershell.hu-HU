---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 3005E411-9466-4602-8E07-F4EF8804AB2A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 22bff485bf49e0ec5f482e1325af661862583605
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015752"
---
# Start-AzureSqlDatabaseExport

## Áttekintés
Az exportálási műveletet egy Azure SQL-adatbázisból blob-tárolóba kezdi.

## SZINTAXISA

### ByContainerObject
```
Start-AzureSqlDatabaseExport -SqlConnectionContext <ISqlServerConnectionInformation>
 -StorageContainer <AzureStorageContainer> -DatabaseName <String> -BlobName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByContainerName
```
Start-AzureSqlDatabaseExport -SqlConnectionContext <ISqlServerConnectionInformation>
 -StorageContext <IStorageContext> -StorageContainerName <String> -DatabaseName <String> -BlobName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **Start-AzureSqlDatabaseExport** parancsmag az Azure SQL-adatbázisból blob-tárolóba kezdi az exportálási műveletet.
A művelethez adatbázis-kiszolgáló kapcsolati környezet szükséges.
Az exportálási művelet állapotának lekérdezéséhez használja az Get-AzureSqlDatabaseImportExportStatus parancsmagot.

## Példák

### 1. példa: adatbázis exportálása
```
PS C:\>$Credential = Get-Credential
PS C:\> $SqlContext = New-AzureSqlDatabaseServerContext -ServerName $ServerName -Credential $Credential
PS C:\> $StorageContext = New-AzureStorageContext -StorageAccountName $StorageName -StorageAccountKey $StorageKey
PS C:\> $Container = Get-AzureStorageContainer -Name $ContainerName -Context $StorageContext
PS C:\> $exportRequest = Start-AzureSqlDatabaseExport -SqlConnectionContext $SqlContext -StorageContainer $Container -DatabaseName $DatabaseName -BlobName $BlobName
```

Ez a példa olyan exportálási folyamatot kezdeményez az Azure SQL-adatbázisból, amely a $DatabaseName változóban tárolt nevet tartalmazza a $BlobName változóban tárolt blob-tárolónak.

## PARAMÉTEREK

### -BlobName
Annak az Azure Blob-tárolónak a nevét adja meg, amelyre a parancsmag az adatbázist exportálja.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DatabaseName
Annak az adatbázisnak a nevét adja meg, amelyből a parancsmag az adatot exportálja.

```yaml
Type: String
Parameter Sets: (All)
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

### -SqlConnectionContext
Az adatbázist tartalmazó kiszolgáló kapcsolati környezetét adja meg.

```yaml
Type: ISqlServerConnectionInformation
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageContainer
Annak a tárolónak a tárolóját adja meg, amely a parancsmagot tartalmazó blobot exportálja.

```yaml
Type: AzureStorageContainer
Parameter Sets: ByContainerObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageContainerName
Annak a tárolónak a nevét adja meg, amely a parancsmagot tartalmazó blobot exportálja.

```yaml
Type: String
Parameter Sets: ByContainerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageContext
A blob-tároló tároló környezetét adja meg.

```yaml
Type: IStorageContext
Parameter Sets: ByContainerName
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

### Microsoft. WindowsAzure. Command. SqlDatabase. Services. ImportExportRequest

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Azure SQL-adatbázis](https://azure.microsoft.com/en-us/services/sql-database/)

[Adatbázis exportálása](https://msdn.microsoft.com/en-us/library/azure/dn781282.aspx)

[Azure SQL-adatbázisok műveletei](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Get-AzureSqlDatabaseImportExportStatus](./Get-AzureSqlDatabaseImportExportStatus.md)

[Start-AzureSqlDatabaseImport](./Start-AzureSqlDatabaseImport.md)


