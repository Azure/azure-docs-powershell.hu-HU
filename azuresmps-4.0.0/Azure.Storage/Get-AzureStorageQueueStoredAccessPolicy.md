---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: F1EC601C-3ADD-402A-A5F7-84A95D312187
online version: ''
schema: 2.0.0
ms.openlocfilehash: 552b1e638034cf0cec5825b742af4984b688cec3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491728"
---
# Get-AzureStorageQueueStoredAccessPolicy

## Áttekintés
Beolvassa a tárolt hozzáférési házirendet vagy házirendet egy Azure-tárterület várólistájához.

## SZINTAXISA

```
Get-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## Leírás
A **Get-AzureStorageQueueStoredAccessPolicy** parancsmag felsorolja az Azure-tárterületek várólistájának tárolt elérési házirendjét vagy házirendjeit.

## Példák

### 1. példa: tárolt hozzáférési házirend beszerzése a várólistában
```
PS C:\>Get-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy12"
```

Ez a parancs a Policy12 nevű Access-házirendet a MyQueue nevű tárolási várólistában kapja meg.

### 2. példa: az összes tárolt Access-házirend beolvasása a várólistán
```
PS C:\>Get-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue"
```

Ez a parancs a MyQueue nevű várólistában minden tárolt Access-házirendet beolvas.

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

### -Queue (várólista)
Az Azure Storage Queue nevet adja meg.

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

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzureStorageQueueStoredAccessPolicy](./New-AzureStorageQueueStoredAccessPolicy.md)

[Remove-AzureStorageQueueStoredAccessPolicy](./Remove-AzureStorageQueueStoredAccessPolicy.md)

[Set-AzureStorageQueueStoredAccessPolicy](./Set-AzureStorageQueueStoredAccessPolicy.md)

[Új – AzureStorageContext](./New-AzureStorageContext.md)


