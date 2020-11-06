---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BDF42420-3616-4A64-9562-1A896F828728
online version: ''
schema: 2.0.0
ms.openlocfilehash: 427276a496108a48b69fd81cb5835d74859c25b4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491332"
---
# New-AzureStorageShareSASToken

## Áttekintés
Megosztott hozzáférés-aláírási jogkivonat létrehozása az Azure tárhely-megosztásához.

## SZINTAXISA

### SasPolicy
```
New-AzureStorageShareSASToken [-ShareName] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### SasPermission
```
New-AzureStorageShareSASToken [-ShareName] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## Leírás
A **New-AzureStorageShareSASToken** parancsmag létrehoz egy Access-aláírási jogkivonatot egy Azure-tárterület-megosztáshoz.

## Példák

### Példa 1: megosztott hozzáférés-aláírási jogkivonat létrehozása megosztáshoz
```
PS C:\>New-AzureStorageShareSASToken -ShareName "ContosoShare" -Permission "rwdl"
```

Ez a parancs létrehoz egy megosztott Access-aláírási tokent a ContosoShare nevű megosztáshoz.

### 2. példa: több megosztott hozzáférés-aláírási jogkivonat létrehozása a csővezeték használatával
```
PS C:\>Get-AzureStorageShare -Prefix "test" | New-AzureStorageShareSASToken -Permission "rwdl"
```

Ez a parancs beilleszti az előtag-teszthez tartozó összes tárolási megosztást.
A parancs a csővezeték-kezelő segítségével átadja őket az aktuális parancsmagnak.
Az aktuális parancsmag létrehoz egy megosztott hozzáférési jogkivonatot minden olyan tárterülethez, amely a megadott engedélyekkel rendelkezik.

### 3. példa: egy megosztott hozzáférés-vezérlőt használó, megosztott hozzáférésű aláírási jogkivonat létrehozása
```
PS C:\>New-AzureStorageShareSASToken -ShareName "ContosoShare" -Policy "ContosoPolicy03"
```

Ez a parancs létrehoz egy megosztott Access-aláírási jogkivonatot a ContosoShare nevű tároló-megosztáshoz, amely a ContosoPolicy03 nevű házirenddel rendelkezik.

## PARAMÉTEREK

### -Környezet
Az Azure tárolási környezetét adja meg.
Környezet beolvasásához használja az New-AzureStorageContext parancsmagot.

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ExpiryTime
Azt az időpontot adja meg, amikor a megosztott elérési aláírás érvénytelenné válik.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FullUri
Jelzi, hogy ez a parancsmag a teljes blob URI-t és a megosztott hozzáférés-aláírási tokent adja vissza.

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

### -IPAddressOrRange
Adja meg az IP-címet vagy az IP-címeket, amelyekből el szeretné fogadni a kéréseket, például a 168.1.5.65 vagy a 168.1.5.60-168.1.5.70.
A tartomány bezárólag.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### – Engedély
A jogkivonatban található engedélyeket a megosztás alatti megosztás és fájlok eléréséhez adja meg.

```yaml
Type: String
Parameter Sets: SasPermission
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Házirend
Megadhatja a megosztáshoz tartozó tárolt hozzáférés-házirendet.

```yaml
Type: String
Parameter Sets: SasPolicy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Protocol
A kéréshez engedélyezett protokollt adja meg.
A paraméter elfogadható értékei a következők:
* HttpsOnly
* HttpsOrHttp

Az alapértelmezett érték a HttpsOrHttp.

```yaml
Type: SharedAccessProtocol
Parameter Sets: (All)
Aliases: 
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Megosztásnév
A tárolási megosztás nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Kezdő időpont
Azt az időpontot adja meg, amikor a megosztott hozzáférés aláírása érvényes lesz.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI
* Kulcsszavak: gyakori, Azure, Services, Data, Storage, blob, queue, Table

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureStorageShare](./Get-AzureStorageShare.md)

[Új – AzureStorageFileSASToken](./New-AzureStorageFileSASToken.md)
