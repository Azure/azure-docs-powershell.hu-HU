---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3B5B828A-6B3E-49BD-8BA9-916F8B69B8E9
online version: ''
schema: 2.0.0
ms.openlocfilehash: b9117d5a4149842ffd136caf1c986c70a4b5e187
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491722"
---
# Get-AzureStorageServiceMetricsProperty

## Áttekintés
Az Azure Storage szolgáltatás metrikájának tulajdonságai

## SZINTAXISA

```
Get-AzureStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Context <IStorageContext>] [<CommonParameters>]
```

## Leírás
A **Get-AzureStorageServiceMetricsProperty** parancsmag metrikák tulajdonságait az Azure Storage szolgáltatáshoz.

## Példák

### 1. példa: a blob-szolgáltatás metrikák tulajdonságainak beolvasása
```
C:\PS>Get-AzureStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour
```

Ennek a parancsnak a metrikák típusa esetén a blob-tárolóra vonatkozó tulajdonságokat kell kinéznie.

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

### -MetricsType
A mérőszám típusát adja meg.
Ez a parancsmag az Azure Storage Service metrikájának tulajdonságait adja meg a mérőszámok típusához, amelyet ez a paraméter határoz meg.
A paraméter elfogadható értékei a következők: óra és perc.

```yaml
Type: ServiceMetricsType
Parameter Sets: (All)
Aliases: 
Accepted values: Hour, Minute

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceType
A tárterület szolgáltatás típusát adja meg.
Ez a parancsmag a paraméter által megadott típus metrikájának tulajdonságait adja meg.
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

[Set-AzureStorageServiceMetricsProperty](./Set-AzureStorageServiceMetricsProperty.md)


