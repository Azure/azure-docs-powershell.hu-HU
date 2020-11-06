---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 4631D36F-926A-4279-AA4D-5F694C18081E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3f2bccab190fc27b5e97ecf3af502d3488f28998
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491715"
---
# Get-AzureStorageTable

## Áttekintés
A tárolási táblák listája.

## SZINTAXISA

### Táblanév (alapértelmezett)
```
Get-AzureStorageTable [[-Name] <String>] [-Context <IStorageContext>] [<CommonParameters>]
```

### TablePrefix
```
Get-AzureStorageTable -Prefix <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## Leírás
A **Get-AzureStorageTable** parancsmag az Azure-beli tárterület-fiókkal társított tárolási táblákat sorolja fel.

## Példák

### 1. példa: az összes Azure Storage Table listázása
```
PS C:\>Get-AzureStorageTable
```

Ez a parancs a tárterület-fiókok minden tárolási tábláját beilleszti.

### 2. példa: az Azure Storage Tables listázása helyettesítő karakterrel
```
PS C:\>Get-AzureStorageTable -Name table*
```

Ez a parancs egy helyettesítő karaktert használ az olyan tárolási táblák beszerzéséhez, amelyek neve táblázattal kezdődik.

### 3. példa: az Azure Storage Tables listázása táblanév előtaggal
```
PS C:\>Get-AzureStorageTable -Prefix "table"
```

Ez a parancs az *előtag* paraméterrel olyan tárolási táblákat kap, amelyeknek a neve táblázattal kezdődik.

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
A táblázat nevét adja meg.
Ha a táblázat neve üres, a parancsmag felsorolja az összes táblázatot.
Ellenkező esetben az összes olyan táblát felsorolja, amely megfelel a megadott névnek vagy a normál név mintának.

```yaml
Type: String
Parameter Sets: TableName
Aliases: N, Table

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Prefix
A bekapni kívánt tábla vagy táblák nevében használt előtagot adja meg.
Ezzel az eszközzel megkeresheti az összes olyan táblát, amely ugyanazzal a karakterlánccal kezdődik, mint amilyen például a táblázat.

```yaml
Type: String
Parameter Sets: TablePrefix
Aliases: 

Required: True
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

[Új – AzureStorageTable](./New-AzureStorageTable.md)

[Remove-AzureStorageTable](./Remove-AzureStorageTable.md)


