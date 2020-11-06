---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3B4F32F3-51ED-4851-B38F-172658186C96
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9a58f869d5308b176a68614cbb2fa2fec401fa14
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491612"
---
# New-AzureStorageTable

## Áttekintés
Tároló táblát hoz létre.

## SZINTAXISA

```
New-AzureStorageTable [-Name] <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## Leírás
A **New-AzureStorageTable** parancsmag létrehoz egy tárterület-táblát az Azure-ban tárolt tárolási fiókhoz társítva.

## Példák

### 1. példa: Azure Storage Table létrehozása
```
PS C:\>New-AzureStorageTable -Name "tableabc"
```

A parancs létrehozza a tableabc nevű tárterület-táblázatot.

### 2. példa: több Azure Storage-tábla létrehozása
```
PS C:\>"table1 table2 table3".split() | New-AzureStorageTable
```

A parancs több táblát hoz létre.
A .NET **String** osztály **felosztott** metódusát használja, és a neveket átadja a csővezetéken.

## PARAMÉTEREK

### -Környezet
A tárolási környezetet adja meg.
A létrehozáshoz használhatja az New-AzureStorageContext parancsmagot.

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
Az új tábla nevét adja meg.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureStorageTable](./Get-AzureStorageTable.md)

[Remove-AzureStorageTable](./Remove-AzureStorageTable.md)


