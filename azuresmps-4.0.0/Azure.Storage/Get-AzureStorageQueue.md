---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C2EBCCF0-56CE-4D49-A138-74E52FC3A9AC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 11a8ffe26a65bf2ecabab7807d8e54bc23b629fc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491729"
---
# Get-AzureStorageQueue

## Áttekintés
A tárolási várólisták listája.

## SZINTAXISA

### QueueName (alapértelmezett)
```
Get-AzureStorageQueue [[-Name] <String>] [-Context <IStorageContext>] [<CommonParameters>]
```

### QueuePrefix
```
Get-AzureStorageQueue -Prefix <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## Leírás
A **Get-AzureStorageQueue** parancsmag az Azure tárterület-fiókjához társított tárolási várólistákat sorolja fel.

## Példák

### 1. példa: az összes Azure-tároló várólistájának listázása
```
PS C:\>Get-AzureStorageQueue
```

Ez a parancs felsorolja az aktuális tárterület-fiók tárolási várólistáit.

### 2. példa: az Azure tárolási várólistái a helyettesítő karakterekkel jelennek meg
```
PS C:\>Get-AzureStorageQueue -Name queue*
```

A parancs egy helyettesítő karaktert használ a tárolási várólisták listájának megjelenítéséhez, amelynek a neve a várólistával fog kezdődni.

### 3. példa: az Azure tárolási várólistái a várólista neve előtag használatával
```
PS C:\>Get-AzureStorageQueue -Prefix "queue"
```

Ebben a példában az *előtag* paraméterrel kilistázhatja azokat a tárolási várólistákat, amelyeknek a neve a várólistával fog kezdődni.

## PARAMÉTEREK

### -Környezet
Az Azure tárolási környezetét adja meg.
Ezt a **New-AzureStorageContext** parancsmag segítségével hozhatja létre.

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
Egy nevet ad meg.
Ha nincs megadva név, a parancsmag felsorolja az összes várólistát.
Ha meg van adva egy teljes vagy részleges név, a parancsmag minden olyan várólistát kap, amely megfelel a név mintának.

```yaml
Type: String
Parameter Sets: QueueName
Aliases: N, Queue

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Prefix
A bekapni kívánt várólisták nevében használt előtagot adja meg.

```yaml
Type: String
Parameter Sets: QueuePrefix
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

[Új – AzureStorageQueue](./New-AzureStorageQueue.md)

[Remove-AzureStorageQueue](./Remove-AzureStorageQueue.md)


