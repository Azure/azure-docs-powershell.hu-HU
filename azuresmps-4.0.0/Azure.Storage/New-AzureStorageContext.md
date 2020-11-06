---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 383402B2-6B7C-41AB-AFF9-36C86156B0A9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4db0b752e8bf887e899a4de6a8e4175eaa2d9855
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491444"
---
# New-AzureStorageContext

## Áttekintés
Azure-tárterületet hoz létre.

## SZINTAXISA

### AccountNameAndKey (alapértelmezett)
```
New-AzureStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### AccountNameAndKeyEnvironment
```
New-AzureStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### AnonymousAccount
```
New-AzureStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] [-Endpoint <String>]
 [<CommonParameters>]
```

### AnonymousAccountEnvironment
```
New-AzureStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] -Environment <String>
 [<CommonParameters>]
```

### SasToken
```
New-AzureStorageContext [-StorageAccountName] <String> -SasToken <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### SasTokenWithAzureEnvironment
```
New-AzureStorageContext [-StorageAccountName] <String> -SasToken <String> -Environment <String>
 [<CommonParameters>]
```

### ConnectionString
```
New-AzureStorageContext -ConnectionString <String> [<CommonParameters>]
```

### LocalDevelopment
```
New-AzureStorageContext [-Local] [<CommonParameters>]
```

## Leírás
A **New-AzureStorageContext** parancsmag Azure-tárterületet hoz létre.

## Példák

### Példa 1: környezet létrehozása tárolási fiók nevének és kulcsának megadásával
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
```

Ez a parancs létrehoz egy környezetet a ContosoGeneral nevű fiókhoz, amely a megadott kulcsot használja.

### 2. példa: környezet létrehozása kapcsolati karakterlánc megadásával
```
C:\PS>New-AzureStorageContext -ConnectionString "DefaultEndpointsProtocol=https;AccountName=ContosoGeneral;AccountKey=< Storage Key for ContosoGeneral ends with == >;"
```

A parancs a megadott kapcsolati karakterláncon alapuló környezetet hoz létre a fiók ContosoGeneral.

### Példa 3: névtelen tárterület-fiók környezetének létrehozása
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -Anonymous -Protocol "http"
```

Ez a parancs a ContosoGeneral nevű fiók névtelen használatára szolgáló környezetét hozza létre.
A parancs a HTTP protokollt adja meg kapcsolati protokollként.

### Példa 4: környezet létrehozása a helyi fejlesztési tárterület-fiók használatával
```
C:\PS>New-AzureStorageContext -Local
```

A parancs a helyi fejlesztési tárterület-fiók segítségével hozza létre a környezetet.
A parancs a *helyi* paramétert adja meg.

### Példa 5: a helyi fejlesztői tárterület-fiók tárolójának beszerzése
```
C:\PS>New-AzureStorageContext -Local | Get-AzureStorageContainer
```

A parancs a helyi fejlesztési tárterület-fiók segítségével hoz létre környezetet, majd átadja az új környezetet a **Get-AzureStorageContainer** parancsmagnak a pipeline operátor használatával.
A parancs az Azure Storage containert kapja meg a helyi fejlesztői tárterület-fiókhoz.

### Példa 6: több tároló beszerzése
```
C:\PS>$Context01 = New-AzureStorageContext -Local 
PS C:\> $Context02 = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
PS C:\> ($Context01, $Context02) | Get-AzureStorageContainer
```

Az első parancs a helyi fejlesztési tárterület-fiók segítségével hoz létre környezetet, majd a $Context 01 változóban tárolja ezt a környezetet.

A második parancs létrehoz egy környezetet a ContosoGeneral nevű fiókhoz, amely a megadott kulcsot használja, majd a környezetet a $Context 02 változóban tárolja.

A végleges parancs a **Get-AzureStorageContainer** a $Context 01-ben és a $Context 02-ban tárolt környezetek tárolóit kapja.

### 7. példa: környezet létrehozása végponttal
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Endpoint "contosoaccount.core.windows.net"
```

A parancs létrehoz egy Azure-tárterületet, amely a megadott tárterület-végponttal rendelkezik.
A parancs létrehozza a ContosoGeneral nevű fiók környezetét, amely a megadott kulcsot használja.

### 8. példa: környezet létrehozása meghatározott környezettel
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Environment "AzureChinaCloud"
```

Ez a parancs olyan Azure-tárterületet hoz létre, amely a megadott Azure-környezettel rendelkezik.
A parancs létrehozza a ContosoGeneral nevű fiók környezetét, amely a megadott kulcsot használja.

### Példa 9: környezet létrehozása SAS-token használatával
```
C:\PS>$SasToken = New-AzureStorageContainerSASToken -Name "ContosoMain" -Permission "raud"
PS C:\> $Context = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -SasToken $SasToken
PS C:\> $Context | Get-AzureStorageBlob -Container "ContosoMain"
```

Az első parancs a ContosoMain nevű tároló **új-AzureStorageContainerSASToken** parancsmagjának segítségével hoz létre egy sas-tokent, majd a tokent a $SasToken változóban tárolja.
Ez a token az olvasási, a hozzáadási, a frissítési és a törlési engedély.

A második parancs létrehoz egy környezetet a ContosoGeneral nevű fiókhoz, amely a $SasTokenban tárolt SAS-jogkivonatot használja, majd a $Context változóban tárolja ezt a környezetet.

A végleges parancs felsorolja a ContosoMain nevű tárolóhoz társított összes blobot az $Context-ben tárolt környezettel.

## PARAMÉTEREK

### -Névtelen
Jelzi, hogy ez a parancsmag Azure-tárterületet hoz létre a névtelen bejelentkezéshez.

```yaml
Type: SwitchParameter
Parameter Sets: AnonymousAccount, AnonymousAccountEnvironment
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConnectionString
Az Azure tárolási környezet kapcsolati karakterláncát adja meg.

```yaml
Type: String
Parameter Sets: ConnectionString
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Végpont
Az Azure tárolási környezet végpontját adja meg.

```yaml
Type: String
Parameter Sets: AccountNameAndKey, AnonymousAccount, SasToken
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Környezet
Az Azure-környezetet adja meg.
A paraméter elfogadható értékei a következők: AzureCloud és AzureChinaCloud.
További információért írja be a következőt: `Get-Help Get-AzureEnvironment` .

```yaml
Type: String
Parameter Sets: AccountNameAndKeyEnvironment, AnonymousAccountEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SasTokenWithAzureEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Local (helyi)
Jelzi, hogy a parancsmag a helyi fejlesztési tárterület-fiók segítségével hoz létre környezetet.

```yaml
Type: SwitchParameter
Parameter Sets: LocalDevelopment
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Protocol
Annak a protokollnak a használatát adja meg, amely a biztonsági fiókkezelő fiókkal végzett kéréshez engedélyezve van.
A paraméter elfogadható értékei a következők:

- HttpsOnly
- HttpsOrHttp

Az alapértelmezett érték a HttpsOrHttp.

```yaml
Type: String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken
Aliases: 
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SasToken
Egy megosztott hozzáférés-aláírási (SAS) tokent ad meg a kontextushoz.

```yaml
Type: String
Parameter Sets: SasToken, SasTokenWithAzureEnvironment
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountKey
Az Azure Storage Account kulcsát adja meg.
Ez a parancsmag létrehoz egy környezetet annak a kulcsnak, amelyet a paraméter határoz meg.

```yaml
Type: String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountName
Az Azure Storage-fiók nevét adja meg.
Ez a parancsmag a paraméter által megadott fiók környezetét adja meg.

```yaml
Type: String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken, SasTokenWithAzureEnvironment
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

### AzureStorageContext

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureStorageBlob](./Get-AzureStorageBlob.md)

[Új – AzureStorageContainerSASToken](./New-AzureStorageContainerSASToken.md)


