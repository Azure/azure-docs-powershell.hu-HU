---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3CFA6E31-E243-4B22-AE8F-1942DD324639
online version: ''
schema: 2.0.0
ms.openlocfilehash: 39870fe9fe9ac4223bccf15908c960db29d25252
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491812"
---
# New-AzureStorageTableSASToken

## Áttekintés
Létrehoz egy SAS-jogkivonatot az Azure Storage-táblájához.

## SZINTAXISA

### SasPolicy
```
New-AzureStorageTableSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### SasPermission
```
New-AzureStorageTableSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## Leírás
A **New-AzureStorageTableSASToken** parancsmag létrehoz egy megosztott Access-aláírási (SAS) tokent az Azure Storage Table-hoz.

## Példák

### Példa 1: olyan SAS-token létrehozása, amely teljes hozzáféréssel rendelkezik a táblázathoz
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Permission "raud"
```

Ez a parancs egy SAS-jogkivonatot hoz létre a ContosoResources nevű táblázat teljes engedélyeivel.
Ez a token az olvasási, a hozzáadási, a frissítési és a törlési engedély.

### 2. példa: egy több partíciót tartalmazó SAS-token létrehozása
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Permission "raud" -StartPartitionKey "a" -EndPartitionKey "b"
```

Ez a parancs a ContosoResources nevű táblára vonatkozó teljes engedélyekkel generálta és a SAS-tokent hozza létre.
A parancs a tokent a *StartPartitionKey* és a *EndPartitionKey* paraméterrel megadott tartományra korlátozza.

### 3. példa: olyan SAS-token létrehozása, amely egy táblához tárolt hozzáférés-házirendet tartalmaz
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Policy "ClientPolicy01"
```

A parancs létrehoz egy SAS-jogkivonatot a ContosoResources nevű táblához.
A parancs a ClientPolicy01 nevű tárolt elérési házirendet adja meg.

## PARAMÉTEREK

### -Környezet
Az Azure tárolási környezetét adja meg.
A tárolási környezet eléréséhez használja az New-AzureStorageContext parancsmagot.

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

### -EndPartitionKey
A parancsmag által létrehozott tokenhez tartozó sor végének a Partition (partíció) kulcsát adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: endpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndRowKey
A parancsmag által létrehozott tokenhez tartozó sor végéhez tartozó sor billentyűt adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: endrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExpiryTime
Azt adja meg, hogy mikor jár le a SAS-jogkivonat.

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
Azt jelzi, hogy ez a parancsmag a teljes várólista-URI azonosítót adja eredményül a SAS-jogkivonattal.

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
Az Azure Storage Table-táblázat nevét adja meg.
Ez a parancsmag létrehoz egy SAS-jogkivonatot annak a táblának, amelyet a paraméter határoz meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### – Engedély
Megadja az Azure Storage Table engedélyeit.

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
A tárolt hozzáférési házirendet adja meg, amely tartalmazza az e SAS-jogkivonat engedélyeit.

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

### -StartPartitionKey
A parancsmag által létrehozott jogkivonat-sor kezdetének a Partition kulcsát adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: startpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartRowKey
A parancsmag által létrehozott jogkivonat-sor kezdetének a sorát adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: startrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Kezdő időpont
Azt adja meg, hogy a SAS-token érvényes lesz.

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

[Új – AzureStorageContext](./New-AzureStorageContext.md)
