---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 76876cb76e65c913401d62fc7f08b3cb8b5626c0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491435"
---
# New-AzureStorageQueue

## Áttekintés
Tárolási várólistát hoz létre.

## SZINTAXISA

```
New-AzureStorageQueue [-Name] <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## Leírás
A **New-AzureStorageQueue** parancsmag létrehoz egy tárolási várólistát az Azure-ban.

## Példák

### Példa 1: Azure Storage Queue létrehozása
```
PS C:\>New-AzureStorageQueue -Name "queueabc"
```

Ez a példa létrehoz egy queueabc nevű tárolási várólistát.

### 2. példa: több Azure-tárterületet tároló várólista létrehozása
```
PS C:\>"queue1 queue2 queue3".split() | New-AzureStorageQueue
```

Ez a példa több tárolási várólistát hoz létre.
A .NET string osztály felosztott metódusát használja, és a neveket átadja a csővezetéken.

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

### -Name (név)
A várólista nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Queue

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

[Get-AzureStorageQueue](./Get-AzureStorageQueue.md)

[Remove-AzureStorageQueue](./Remove-AzureStorageQueue.md)


