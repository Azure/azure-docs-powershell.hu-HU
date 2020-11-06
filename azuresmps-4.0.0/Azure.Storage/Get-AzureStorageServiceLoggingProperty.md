---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 494291A1-D854-4E97-B5EE-27BB5653D97C
online version: ''
schema: 2.0.0
ms.openlocfilehash: d615c0a807c12640f20a72b97a2c11c2efcd5b28
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491725"
---
# Get-AzureStorageServiceLoggingProperty

## Áttekintés
Az Azure Storage Services naplózási tulajdonságait kapja.

## SZINTAXISA

```
Get-AzureStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [<CommonParameters>]
```

## Leírás
A **Get-AzureStorageServiceLoggingProperty** parancsmag az Azure Storage Services naplózási tulajdonságait kapja meg.

## Példák

### Példa 1: a blob-szolgáltatás naplózási tulajdonságainak beolvasása
```
C:\PS>Get-AzureStorageServiceLoggingProperty -ServiceType Blob
```

Ez a parancs a blob-tároló naplózási tulajdonságait kapja meg.

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

### -ServiceType
A tárterület szolgáltatás típusát adja meg.
Ez a parancsmag a paraméter által megadott szolgáltatási típus naplózási tulajdonságait kapja meg.
A paraméter elfogadható értékei a következők:

- BLOB 
- Táblázat
- Várólista
- Fájl

A fájl értéke jelenleg nem támogatott.

```yaml
Type: StorageServiceType
Parameter Sets: (All)
Aliases: 
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
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

[Set-AzureStorageServiceLoggingProperty](./Set-AzureStorageServiceLoggingProperty.md)


