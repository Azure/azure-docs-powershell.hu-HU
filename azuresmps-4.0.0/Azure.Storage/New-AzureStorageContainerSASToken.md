---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 6FF04E82-4921-4F7B-83D0-6997316BC5FD
online version: ''
schema: 2.0.0
ms.openlocfilehash: becdf63590b5c5abc5e7095b96e13586232311d1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491710"
---
# New-AzureStorageContainerSASToken

## Áttekintés
Létrehoz egy SAS-jogkivonatot az Azure Storage tárolóhoz.

## SZINTAXISA

### SasPolicy
```
New-AzureStorageContainerSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### SasPermission
```
New-AzureStorageContainerSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## Leírás
A **New-AzureStorageContainerSASToken** parancsmag létrehoz egy Access-aláírási (SAS) tokent egy Azure-tároló tárolóhoz.

## Példák

### 1. példa: a Container SAS-token létrehozása teljes tároló engedéllyel
```
PS C:\>New-AzureStorageContainerSASToken -Name "Test" -Permission rwdl
```

Ebben a példában egy tároló SAS-tokent hoz létre teljes tároló engedéllyel.

### 2. példa: több Container SAS-token létrehozása csővezetékről
```
PS C:\>Get-AzureStorageContainer -Container test* | New-AzureStorageContainerSASToken -Permission rwdl
```

Ez a példa több Container SAS-tokent hoz létre a csővezeték használatával.

### 3. példa: a Container SAS-token létrehozása megosztott hozzáférési házirenddel
```
PS C:\>New-AzureStorageContainerSASToken -Name "Test" -Policy "PolicyName"
```

Ebben a példában egy tároló SAS-tokent hoz létre a megosztott hozzáférés házirendjével.

## PARAMÉTEREK

### -Környezet
Az Azure tárolási környezetét adja meg.
A New-AzureStorageContext parancsmag használatával is létrehozhatja azt.

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

Ha a felhasználó a kezdési időpontot állítja be, de nem a lejárati időt, a lejárati idő a kezdési időpontra és egy órára van állítva.
Ha sem a kezdési időpont, sem a lejárati idő nincs megadva, a lejárati idő az aktuális időpontra és egy órára van állítva.

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

### -Name (név)
Az Azure Storage Container nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### – Engedély
Megadhatja a tároló tároló engedélyeit.

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
Egy, az Azure által tárolt hozzáférési házirendet adja meg.

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

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzureStorageBlobSASToken](./New-AzureStorageBlobSASToken.md)
