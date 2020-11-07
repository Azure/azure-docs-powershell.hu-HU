---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 383402B2-6B7C-41AB-AFF9-36C86156B0A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageContext.md
ms.openlocfilehash: ae22e6923a03864b9371ccdf5379ef9b6bf5189d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843009"
---
# New-AzStorageContext

## Áttekintés
Azure-tárterületet hoz létre.

## SZINTAXISA

### AccountNameAndKey (alapértelmezett)
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### AccountNameAndKeyEnvironment
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### AnonymousAccount
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] [-Endpoint <String>]
 [<CommonParameters>]
```

### AnonymousAccountEnvironment
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] -Environment <String>
 [<CommonParameters>]
```

### SasToken
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### SasTokenWithAzureEnvironment
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> -Environment <String>
 [<CommonParameters>]
```

### ConnectionString
```
New-AzStorageContext -ConnectionString <String> [<CommonParameters>]
```

### LocalDevelopment
```
New-AzStorageContext [-Local] [<CommonParameters>]
```

## Leírás
A **New-AzStorageContext** parancsmag Azure-tárterületet hoz létre.

## Példák

### Példa 1: környezet létrehozása tárolási fiók nevének és kulcsának megadásával
```
C:\PS>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
```

Ez a parancs létrehoz egy környezetet a ContosoGeneral nevű fiókhoz, amely a megadott kulcsot használja.

### 2. példa: környezet létrehozása kapcsolati karakterlánc megadásával
```
C:\PS>New-AzStorageContext -ConnectionString "DefaultEndpointsProtocol=https;AccountName=ContosoGeneral;AccountKey=< Storage Key for ContosoGeneral ends with == >;"
```

A parancs a megadott kapcsolati karakterláncon alapuló környezetet hoz létre a fiók ContosoGeneral.

### Példa 3: névtelen tárterület-fiók környezetének létrehozása
```
C:\PS>New-AzStorageContext -StorageAccountName "ContosoGeneral" -Anonymous -Protocol "http"
```

Ez a parancs a ContosoGeneral nevű fiók névtelen használatára szolgáló környezetét hozza létre.
A parancs a HTTP protokollt adja meg kapcsolati protokollként.

### Példa 4: környezet létrehozása a helyi fejlesztési tárterület-fiók használatával
```
C:\PS>New-AzStorageContext -Local
```

A parancs a helyi fejlesztési tárterület-fiók segítségével hozza létre a környezetet.
A parancs a *helyi* paramétert adja meg.

### Példa 5: a helyi fejlesztői tárterület-fiók tárolójának beszerzése
```
C:\PS>New-AzStorageContext -Local | Get-AzStorageContainer
```

A parancs a helyi fejlesztési tárterület-fiók segítségével hoz létre környezetet, majd átadja az új környezetet a **Get-AzStorageContainer** parancsmagnak a pipeline operátor használatával.
A parancs az Azure Storage containert kapja meg a helyi fejlesztői tárterület-fiókhoz.

### Példa 6: több tároló beszerzése
```
C:\PS>$Context01 = New-AzStorageContext -Local 
PS C:\> $Context02 = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
PS C:\> ($Context01, $Context02) | Get-AzStorageContainer
```

Az első parancs a helyi fejlesztési tárterület-fiók segítségével hoz létre környezetet, majd a $Context 01 változóban tárolja ezt a környezetet.
A második parancs létrehoz egy környezetet a ContosoGeneral nevű fiókhoz, amely a megadott kulcsot használja, majd a környezetet a $Context 02 változóban tárolja.
A végleges parancs a **Get-AzStorageContainer** a $Context 01-ben és a $Context 02-ban tárolt környezetek tárolóit kapja.

### 7. példa: környezet létrehozása végponttal
```
C:\PS>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Endpoint "contosoaccount.core.windows.net"
```

A parancs létrehoz egy Azure-tárterületet, amely a megadott tárterület-végponttal rendelkezik.
A parancs létrehozza a ContosoGeneral nevű fiók környezetét, amely a megadott kulcsot használja.

### 8. példa: környezet létrehozása meghatározott környezettel
```
C:\PS>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Environment "AzureChinaCloud"
```

Ez a parancs olyan Azure-tárterületet hoz létre, amely a megadott Azure-környezettel rendelkezik.
A parancs létrehozza a ContosoGeneral nevű fiók környezetét, amely a megadott kulcsot használja.

### Példa 9: környezet létrehozása SAS-token használatával
```
C:\PS>$SasToken = New-AzStorageContainerSASToken -Name "ContosoMain" -Permission "rad"
PS C:\> $Context = New-AzStorageContext -StorageAccountName "ContosoGeneral" -SasToken $SasToken
PS C:\> $Context | Get-AzStorageBlob -Container "ContosoMain"
```

Az első parancs a ContosoMain nevű tároló **új-AzStorageContainerSASToken** parancsmagjának segítségével hoz létre egy sas-tokent, majd a tokent a $SasToken változóban tárolja.
Ez a token az olvasási, a hozzáadási, a frissítési és a törlési engedély.
A második parancs létrehoz egy környezetet a ContosoGeneral nevű fiókhoz, amely a $SasTokenban tárolt SAS-jogkivonatot használja, majd a $Context változóban tárolja ezt a környezetet.
A végleges parancs felsorolja a ContosoMain nevű tárolóhoz társított összes blobot az $Context-ben tárolt környezettel.

## PARAMÉTEREK

### -Névtelen
Jelzi, hogy ez a parancsmag Azure-tárterületet hoz létre a névtelen bejelentkezéshez.

```yaml
Type: System.Management.Automation.SwitchParameter
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
Type: System.String
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
Type: System.String
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
Type: System.String
Parameter Sets: AccountNameAndKeyEnvironment, AnonymousAccountEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
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
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LocalDevelopment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Protocol
Átviteli protokoll (https/http).

```yaml
Type: System.String
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
Type: System.String
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
Type: System.String
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
Type: System.String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken, SasTokenWithAzureEnvironment
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

## KIMENETEK

### Microsoft. WindowsAzure. Command. Storage. AzureStorageContext

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzStorageBlob](./Get-AzStorageBlob.md)

[Új – AzStorageContainerSASToken](./New-AzStorageContainerSASToken.md)


