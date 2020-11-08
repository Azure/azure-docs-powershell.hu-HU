---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 5EE936CA-DD9A-4BC6-B835-E22AE633B46D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4bc7c8f39f1bdbd35cfffeb59b3b4f184f30845e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015427"
---
# Start-AzureSqlDatabaseImport

## Áttekintés
Az importálási művelet indítása blob-tárolóról Azure SQL-adatbázisba.

## SZINTAXISA

### ByContainerObject
```
Start-AzureSqlDatabaseImport -SqlConnectionContext <ISqlServerConnectionInformation>
 -StorageContainer <AzureStorageContainer> -DatabaseName <String> -BlobName <String>
 [-Edition <DatabaseEdition>] [-DatabaseMaxSize <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByContainerName
```
Start-AzureSqlDatabaseImport -SqlConnectionContext <ISqlServerConnectionInformation>
 -StorageContext <IStorageContext> -StorageContainerName <String> -DatabaseName <String> -BlobName <String>
 [-Edition <DatabaseEdition>] [-DatabaseMaxSize <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **Start-AzureSqlDatabaseImport** parancsmag az Azure Blob-tárolóból egy Azure SQL-adatbázisba kezdi az importálási műveletet.
Ha az adatbázis nem létezik, akkor ez a parancsmag a megadott méret és kiadás értékekkel hozza létre azt.
A művelethez adatbázis-kiszolgáló kapcsolati környezet szükséges.
Az importálási művelet állapotának lekérdezéséhez használja az Get-AzureSqlDatabaseImportExportStatus parancsmagot.

## Példák

### 1. példa: adatbázis importálása
```
PS C:\>$Credential = Get-Credential
PS C:\> $SqlContext = New-AzureSqlDatabaseServerContext -ServerName $ServerName -Credentials $Credential
PS C:\> $StorageContext = New-AzureStorageContext -StorageAccountName $StorageName -StorageAccountKey $StorageKey
PS C:\> $Container = Get-AzureStorageContainer -Name $ContainerName -Context $StorageContext
PS C:\> $ImportRequest = Start-AzureSqlDatabaseImport -SqlConnectionContext $SqlContext -StorageContainer $Container -DatabaseName $DatabaseName -BlobName $BlobName
```

Ez a példa egy importálási folyamatot kezdeményez a $BlobName változó blob-tárterületéről a DatabaseName nevű Azure SQL-adatbázisba.

## PARAMÉTEREK

### -BlobName
Annak az Azure Blob-tárolónak a neve, amelyből a parancsmag az adatbázist importálja.

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

### -DatabaseMaxSize
Az adatbázis maximális méretét adja meg gigabájtban.
Ha az adatbázis nem létezik, akkor ez a parancsmag a maximális méret alapján hozza létre.
Az elfogadható értékek kiadás alapján eltérőek.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DatabaseName
Az adatbázis nevét adja meg.
Ha az adatbázis nem létezik, akkor ez a parancsmag hozza létre, és hozzárendeli a paraméter által megadott nevet.

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

### – Kiadás
Az adatbázis kiadását adja meg.
Ha az adatbázis nem létezik, ez a parancsmag ezt a kiadást hozza létre.
Az érvényes értékek a következők: 

- Nincs
- Web 
- Vállalati verzió 
- Egyszerű
- Standard
- Prémium verzió

Az alapértelmezett a web.

```yaml
Type: DatabaseEdition
Parameter Sets: (All)
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
Annak a tárolónak a tárolóját adja meg, amelyből a parancsmag adatbázis-importálási lehetőséget tartalmaz.

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
A blob-tároló tárolójának a nevét adja meg.

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

[Adatbázis importálása](https://msdn.microsoft.com/en-us/library/azure/dn781284.aspx)

[Azure SQL-adatbázisok műveletei](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Get-AzureSqlDatabaseImportExportStatus](./Get-AzureSqlDatabaseImportExportStatus.md)

[Start-AzureSqlDatabaseExport](./Start-AzureSqlDatabaseExport.md)


