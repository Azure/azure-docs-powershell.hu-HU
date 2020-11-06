---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 37E76360-B683-407C-9AEF-7138374562D8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageShareStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 49d966c23569080ab72d0793014fe4fa5dd71b55
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492639"
---
# New-AzureStorageShareStoredAccessPolicy

## Áttekintés
Tárolt hozzáférési házirendet hoz létre egy tárterület-megosztásban.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

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

### IStorageContext

A "környezet" paraméter elfogadja a "IStorageContext" típusú értéket a csővezetékről

### Karakterlánc

A "megosztásnév" paraméter elfogadja a "string" típusú értéket a csővezetékről

## KIMENETEK

### System. String

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureStorageShareStoredAccessPolicy](./Get-AzureStorageShareStoredAccessPolicy.md)

[Új – AzureStorageContext](./New-AzureStorageContext.md)

[Remove-AzureStorageShareStoredAccessPolicy](./Remove-AzureStorageShareStoredAccessPolicy.md)

[Set-AzureStorageShareStoredAccessPolicy](./Set-AzureStorageShareStoredAccessPolicy.md)
