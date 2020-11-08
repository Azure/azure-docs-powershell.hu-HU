---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B7B29875-D2E5-4E96-AD4B-83032AB18D02
online version: ''
schema: 2.0.0
ms.openlocfilehash: cdcd4788e3eefdce858cb88c0bf1885353f8a673
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015970"
---
# New-AzureSqlDatabaseServerContext

## Áttekintés
Kiszolgáló-kapcsolati környezetet hoz létre.

## SZINTAXISA

### ByServerNameWithSqlAuth (alapértelmezett)
```
New-AzureSqlDatabaseServerContext -ServerName <String> -Credential <PSCredential> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### ByManageUrlWithSqlAuth
```
New-AzureSqlDatabaseServerContext [-ServerName <String>] -ManageUrl <Uri> -Credential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByServerNameWithCertAuth
```
New-AzureSqlDatabaseServerContext -ServerName <String> [-UseSubscription] [-SubscriptionName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByFullyQualifiedServerNameWithSqlAuth
```
New-AzureSqlDatabaseServerContext -FullyQualifiedServerName <String> -Credential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByFullyQualifiedServerNameWithCertAuth
```
New-AzureSqlDatabaseServerContext -FullyQualifiedServerName <String> [-UseSubscription]
 [-SubscriptionName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **New-AzureSqlDatabaseServerContext** parancsmag az Azure SQL Database Server kapcsolati környezetét hozza létre.
SQL Server-hitelesítéssel kapcsolati környezetet hozhat létre egy SQL-adatbázis-kiszolgálóhoz a megadott hitelesítő adatokkal.
Az SQL-adatbázis kiszolgálóját név szerint is megadhatja a teljesen minősített név vagy URL-cím alapján.
A hitelesítő adatok megadásához használja a Get-Credential parancsmagot, amely a Felhasználónév és a jelszó megadását kéri.

Használja a **New-AzureSqlDatabaseServerContext** parancsmagot tanúsítvány-alapú hitelesítéssel a megadott SQL-adatbázis-kiszolgálóhoz való kapcsolódási környezet létrehozásához a megadott Azure-előfizetési adatok használatával.
Az SQL-adatbázis kiszolgálóját név vagy a teljesen minősített név szerint is megadhatja.
Az előfizetési adattípusokat paraméterként adhatja meg, vagy az aktuális Azure-előfizetésből beolvashatja.
Az https://msdn.microsoft.com/library/windowsazure/jj152833.aspx aktuális Azure-előfizetés kiválasztásához használja a Select-AzureSubscription parancsmagot.

## Példák

### Példa 1: környezet létrehozása SQL Server-hitelesítés használatával
```
PS C:\> $Credential = Get-Credential
PS C:\> $Context = New-AzureSqlDatabaseServerContext -ServerName "lpqd0zbr8y" -Credential $Credential
PS C:\> $Database17 = New-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database17" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

Ez a példa az SQL Server-hitelesítést használja.

Az első parancs kéri a kiszolgáló-rendszergazdai hitelesítő adatok megadását, és a hitelesítő adatokat a $Credential változóban tárolja.

A második parancs a lpqd0zbr8y nevű SQL adatbázis-kiszolgálóhoz csatlakozik a $Credential használatával.

A végleges parancs létrehoz egy Database17 nevű adatbázist a kiszolgálón, amely az $Context környezet részét képezi.

### 2. példa: környezet létrehozása tanúsítvány-alapú hitelesítés használatával
```
PS C:\> $SubscriptionId = <Subscription ID>
PS C:\> $Thumbprint = <Certificate Thumbprint>
PS C:\> $Certificate = Get-Item "Cert:\CurrentUser\My\$Thumbprint"
PS C:\> Set-AzureSubscription -SubscriptionName "Subscription07" -SubscriptionId $SubscriptionId -Certificate $Certificate
PS C:\> Select-AzureSubscription -SubscriptionName "Subscription07"
PS C:\> $Context = New-AzureSqlDatabaseServerContext -ServerName "lpqd0zbr8y" -UseSubscription
```

Ez a példa a tanúsítványon alapuló hitelesítést használja.

Az első két parancs az értékekhez rendeli az $SubscriptionId és $Thumbprint változókat.

A harmadik parancs a $Thumbprint ujjlenyomatával azonosított tanúsítványt kapja, és a $Certificate tárolja.

A negyedik parancs beállítja a Subscription07 előfizetést, és az ötödik parancs kiválasztja az előfizetést.

A végleges parancs létrehoz egy környezetet a lpqd0zbr8y nevű kiszolgálóhoz tartozó jelenlegi előfizetésben.

## PARAMÉTEREK

### -Hitelesítő adatok
Megadja azt a hitelesítőadat-objektumot, amely SQL Server-hitelesítést nyújt Önnek a kiszolgáló eléréséhez.

```yaml
Type: PSCredential
Parameter Sets: ByServerNameWithSqlAuth, ByManageUrlWithSqlAuth, ByFullyQualifiedServerNameWithSqlAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FullyQualifiedServerName
Az Azure SQL Server-kiszolgáló teljes tartománynevét (FQDN) tartalmazó nevet adja meg.
Például Server02.database.windows.net.

```yaml
Type: String
Parameter Sets: ByFullyQualifiedServerNameWithSqlAuth, ByFullyQualifiedServerNameWithCertAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManageUrl
Megadja, hogy a parancsmag milyen URL-címet használ az Azure SQL DatabaseManagement-portál eléréséhez a kiszolgálón.

```yaml
Type: Uri
Parameter Sets: ByManageUrlWithSqlAuth
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

### -Kiszolgálónév
Az adatbázis-kiszolgáló nevét adja meg.

```yaml
Type: String
Parameter Sets: ByServerNameWithSqlAuth, ByServerNameWithCertAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByManageUrlWithSqlAuth
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubscriptionName
Megadja annak az Azure-előfizetésnek a nevét, amelyet a parancsmag a kapcsolati környezet létrehozásához használ.
Ha nem ad meg értéket ehhez a paraméterhez, a parancsmag az aktuális előfizetést használja.
Az aktuális előfizetés módosításához futtassa az Select-AzureSubscription parancsmagot.

```yaml
Type: String
Parameter Sets: ByServerNameWithCertAuth, ByFullyQualifiedServerNameWithCertAuth
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UseSubscription
Jelzi, hogy ez a parancsmag Azure-előfizetést használ a kapcsolati környezet létrehozásához.

```yaml
Type: SwitchParameter
Parameter Sets: ByServerNameWithCertAuth, ByFullyQualifiedServerNameWithCertAuth
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

### Microsoft. WindowsAzure. Command. SqlDatabase. Services. Server. IServerDataServiceContext

## MEGJEGYZI
* Ha tartomány megadása nélkül hitelesíti magát, és Windows PowerShell 2,0-t használ, a Get-Credential parancsmag a \\ felhasználónévhez tartozó fordított () egységprefixumokat ad eredményül, például \User. A Windows PowerShell 3,0 nem adja hozzá a fordított perjelet. Ezt a fordított perjelet a **New-AzureSqlDatabaseServerContext** parancsmag *hitelesítő* paramétere nem ismeri fel. Az eltávolításhoz az alábbihoz hasonló parancsok használhatók:

  `PS C:\\\> $Credential = Get-Credential`
`PS C:\\\> $Credential = New-Object -TypeName 'System.Management.Automation.PSCredential' -ArgumentList $Credential.Username.Replace("\",""),$Credential.Password`

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Azure SQL-adatbázis-parancsmagok](./Azure.SQLDatabase.md)

[Get-AzureSqlDatabase](./Get-AzureSqlDatabase.md)

[Új – AzureSqlDatabase](./New-AzureSqlDatabase.md)

[Remove-AzureSqlDatabase](./Remove-AzureSqlDatabase.md)

[Set-AzureSqlDatabase](./Set-AzureSqlDatabase.md)


