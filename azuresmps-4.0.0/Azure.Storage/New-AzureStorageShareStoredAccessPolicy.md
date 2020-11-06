---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 37E76360-B683-407C-9AEF-7138374562D8
online version: ''
schema: 2.0.0
ms.openlocfilehash: f76cd56055e800dc5d7d5ac15e66be23621ffbe2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491092"
---
# New-AzureStorageShareStoredAccessPolicy

## Áttekintés
Tárolt hozzáférési házirendet hoz létre egy tárterület-megosztásban.

## SZINTAXISA

```
New-AzureStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## Leírás
A **New-AzureStorageShareStoredAccessPolicy** parancsmag létrehoz egy tárolt hozzáférési házirendet egy Azure-tárhelyen.

## Példák

### Példa 1: tárolt hozzáférés-házirend létrehozása egy megosztásban
```
PS C:\>New-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy" -Permission "rwdl"
```

Ez a parancs egy olyan tárolt hozzáférési házirendet hoz létre, amely teljes hozzáféréssel rendelkezik a megosztásban.

## PARAMÉTEREK

### -ClientTimeoutPerRequest
Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.
Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.
Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.

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

### -ConcurrentTaskCount
A párhuzamos hálózati hívásokat adja meg.
Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.
A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.
Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).
Az alapértelmezett érték 10.

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

### -Környezet
Az Azure tárolási környezetét adja meg.
A tárolási környezet eléréséhez használja a [New-AzureStorageContext](./New-AzureStorageContext.md) parancsmagot.

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
Azt az időpontot adja meg, amikor a tárolt hozzáférési házirend érvénytelenné válik.

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

### – Engedély
A tárolt elérési házirend engedélyeinek megadása a tárterület-megosztás vagy-fájlok eléréséhez.

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

### -Házirend
A tárolt hozzáférési házirend nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
A kérés kiszolgálói részének időtúllépési időszakát adja meg.

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
Azt az időpontot adja meg, amikor a tárolt hozzáférési házirend érvényes lesz.

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

[Get-AzureStorageShareStoredAccessPolicy](./Get-AzureStorageShareStoredAccessPolicy.md)

[Új – AzureStorageContext](./New-AzureStorageContext.md)

[Remove-AzureStorageShareStoredAccessPolicy](./Remove-AzureStorageShareStoredAccessPolicy.md)

[Set-AzureStorageShareStoredAccessPolicy](./Set-AzureStorageShareStoredAccessPolicy.md)
