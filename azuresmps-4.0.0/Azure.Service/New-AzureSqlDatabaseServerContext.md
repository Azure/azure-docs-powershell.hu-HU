---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B7B29875-D2E5-4E96-AD4B-83032AB18D02
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5312556cb49d02ea901b4cb2526a36f7237f66d1
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100404173"
---
# New-AzureSqlDatabaseServerContext

## SYNOPSIS
Kiszolgálókapcsolat környezetét hozza létre.

## SZINTAXIS

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

## LEÍRÁS
A **New-AzureSqlDatabaseServerContext** parancsmag létrehoz egy Azure SQL Database Server-kapcsolatkörnyezetet.
Az SQL Server-hitelesítéssel kapcsolatot hozhat létre egy SQL-adatbázis-kiszolgálóval a megadott hitelesítő adatokkal.
Az SQL-adatbázis-kiszolgálót név, teljes név vagy URL-cím szerint is megadhatja.
Hitelesítő adatok beszerzéséhez használja a Get-Credential parancsmagot, amely a felhasználónév és a jelszó megadására kéri.

A **New-AzureSqlDatabaseServerContext** parancsmag tanúsítványalapú hitelesítéssel való használatával kapcsolatot hozhat létre a megadott SQL Database-kiszolgálóval a megadott Azure-előfizetési adatok használatával.
Az SQL-adatbázis kiszolgálóját név vagy teljesen minősített név szerint is megadhatja.
Az előfizetés adatait megadhatja paraméterként, vagy lekérheti az aktuális Azure-előfizetésből.
Az aktuális Azure-előfizetés kiválasztásához használja a https://msdn.microsoft.com/library/windowsazure/jj152833.aspx Select-AzureSubscription parancsmagot.

## PÉLDÁK

### 1. példa: Környezet létrehozása SQL Server-hitelesítéssel
```
PS C:\> $Credential = Get-Credential
PS C:\> $Context = New-AzureSqlDatabaseServerContext -ServerName "lpqd0zbr8y" -Credential $Credential
PS C:\> $Database17 = New-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database17" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

Ez a példa SQL Server-hitelesítést használ.

Az első parancs a kiszolgáló rendszergazdájának hitelesítő adatait kéri, és a hitelesítő adatokat a $Credential tárolja.

A második parancs az lpqd0zbr8y nevű SQL Database-kiszolgálóhoz csatlakozik az $Credential.

Az utolsó parancs létrehoz egy Adatbázis17 nevű adatbázist a kiszolgálón, amely a helyi környezet $Context.

### 2. példa: Környezet létrehozása tanúsítványalapú hitelesítéssel
```
PS C:\> $SubscriptionId = <Subscription ID>
PS C:\> $Thumbprint = <Certificate Thumbprint>
PS C:\> $Certificate = Get-Item "Cert:\CurrentUser\My\$Thumbprint"
PS C:\> Set-AzureSubscription -SubscriptionName "Subscription07" -SubscriptionId $SubscriptionId -Certificate $Certificate
PS C:\> Select-AzureSubscription -SubscriptionName "Subscription07"
PS C:\> $Context = New-AzureSqlDatabaseServerContext -ServerName "lpqd0zbr8y" -UseSubscription
```

Ez a példa a tanúsítványalapú hitelesítést használja.

Az első két parancs értékeket rendel a $SubscriptionId és $Thumbprint változókhoz.

A harmadik parancs a tanúsítványt a $Thumbprint azonosítja, és $Certificate.

A negyedik parancs az előfizetést Előfizetés07-re állítja, az ötödik parancs pedig az előfizetést választja ki.

Az utolsó parancs létrehoz egy kontextust az aktuális előfizetésben az lpqd0zbr8y nevű kiszolgálóhoz.

## PARAMETERS

### -Hitelesítő adatok
Egy hitelesítőadat-objektumot ad meg, amely SQL Server-hitelesítést biztosít a kiszolgáló eléréséhez.

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
Az Azure SQL-adatbázis kiszolgálójának teljes tartománynevét (FQDN) adja meg.
Például: Server02.database.windows.net.

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
A parancsmag által a kiszolgáló Azure SQL DatabaseManagement Portáljának eléréséhez használt URL-cím.

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
Azt az Azure-profilt adja meg, amelyből a parancsmag olvas.
Ha nem ad meg profilt, ez a parancsmag a helyi alapértelmezett profilból olvassa be.

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

### -ServerName
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
Megadja annak az Azure-előfizetésnek a nevét, amelyből a parancsmag létrehozza a kapcsolat kontextusát.
Ha nem ad meg értéket ehhez a paraméterhez, a parancsmag az aktuális előfizetést használja.
Az aktuális előfizetés Select-AzureSubscription a Select-AzureSubscription parancsmag futtatásával.

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
Azt jelzi, hogy ez a parancsmag Azure-előfizetést használ a kapcsolat környezetének létrehozására.

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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

## KIMENETEK

### Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.IServerDataServiceContext

## MEGJEGYZÉSEK
* Ha tartomány megadása nélkül hitelesít, és Windows PowerShell 2.0-t használ, a Get-Credential-parancsmag egy, a felhasználónévhez előrendelt törtjelet () ad vissza, például \\ \user. A Windows PowerShell 3.0 nem adja hozzá a perjelet. A törtjelet nem ismeri  fel a **New-AzureSqlDatabaseServerContext** parancsmag hitelesítőadat-paramétere. Az eltávolításához az alábbihoz hasonló parancsokat kell használnia:

  `PS C:\\\> $Credential = Get-Credential`
`PS C:\\\> $Credential = New-Object -TypeName 'System.Management.Automation.PSCredential' -ArgumentList $Credential.Username.Replace("\",""),$Credential.Password`

## KAPCSOLÓDÓ HIVATKOZÁSOK



[Get-AzureSqlDatabase](./Get-AzureSqlDatabase.md)

[New-AzureSqlDatabase](./New-AzureSqlDatabase.md)

[Remove-AzureSqlDatabase](./Remove-AzureSqlDatabase.md)

[Set-AzureSqlDatabase](./Set-AzureSqlDatabase.md)


