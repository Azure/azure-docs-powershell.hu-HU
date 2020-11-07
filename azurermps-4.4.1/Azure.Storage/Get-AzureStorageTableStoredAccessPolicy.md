---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BF5526C1-11B9-47A8-A5A6-CB275B470A9E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageTableStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 85501affef70ce0cf31e62f9083d5ed383425497
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672081"
---
# Get-AzureStorageTableStoredAccessPolicy

## Áttekintés
Beolvassa a tárolt hozzáférési házirendet vagy házirendet egy Azure Storage table.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Get-AzureStorageTableStoredAccessPolicy [-Table] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## Leírás
A **Get-AzureStorageTableStoredAccessPolicy** parancsmag felsorolja az Azure Storage Tables tárolt hozzáférési házirendjét vagy házirendjeit.

## Példák

### Példa 1: tárolt hozzáférés-házirend beszerzése tárterület-táblában
```
PS C:\>Get-AzureStorageTableStoredAccessPolicy -Table "Table02" -Policy "Policy50"
```

Ez a parancs a Policy50 nevű Access-házirendet a Table02 nevű tárolási táblában kapja meg.

### 2. példa: az összes tárolt Access-házirend beolvasása egy tárterület-táblában
```
PS C:\>Get-AzureStorageTableStoredAccessPolicy -Table "Table02"
```

Ez a parancs a Table02 nevű táblázat minden hozzáférési házirendjét bekapja.

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

### -Házirend
A tárolt Access-házirendet adja meg, amely tartalmazza az ehhez a megosztott hozzáférés-aláírási tokenhez tartozó engedélyeket.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Table
Az Azure Storage táblanév nevét adja meg.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### IStorageContext

A "környezet" paraméter elfogadja a "IStorageContext" típusú értéket a csővezetékről

### Karakterlánc

A ' Table ' paraméter elfogadja a "string" típusú értéket a csővezetékről

## KIMENETEK

### Microsoft. WindowsAzure. Storage. table. SharedAccessTablePolicy

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzureStorageTableStoredAccessPolicy](./New-AzureStorageTableStoredAccessPolicy.md)

[Remove-AzureStorageTableStoredAccessPolicy](./Remove-AzureStorageTableStoredAccessPolicy.md)

[Set-AzureStorageTableStoredAccessPolicy](./Set-AzureStorageTableStoredAccessPolicy.md)

[Új – AzureStorageContext](./New-AzureStorageContext.md)


