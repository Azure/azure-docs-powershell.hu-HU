---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 5878FAD4-A4BB-4DBF-A1F2-221FD34F0308
online version: ''
schema: 2.0.0
ms.openlocfilehash: 51921a7d67cd8a297f5cd61716362f13cef6cdc9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491780"
---
# Set-AzureStorageServiceMetricsProperty

## Áttekintés
Módosítja az Azure Storage szolgáltatás metrikák tulajdonságát.

## SZINTAXISA

```
Set-AzureStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Version <Double>] [-RetentionDays <Int32>] [-MetricsLevel <MetricsLevel>] [-PassThru]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## Leírás
A **set-AzureStorageServiceMetricsProperty** parancsmag módosítja az Azure Storage szolgáltatás metrikák tulajdonságát.

## Példák

### 1. példa: a blob-szolgáltatás metrikák tulajdonságainak módosítása
```
C:\PS>Set-AzureStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour -MetricsLevel Service -PassThru -RetentionDays 10 -Version 1.0
```

Ez a parancs a 1,0-os metrikákat a blob-tárolók számára a szolgáltatás szintjére módosítja.
Az Azure Storage Service metrikája 10 napra megőrzi a bejegyzéseket.
Mivel a parancs a *PassThru* paramétert adja meg, a parancs a módosított metrikák tulajdonságot jeleníti meg.

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

### -MetricsLevel
Az Azure-tárterület által a szolgáltatáshoz használt metrikák szintjét adja meg.
A paraméter elfogadható értékei a következők:

- Nincs
- Szolgáltatás
- ServiceAndApi

```yaml
Type: MetricsLevel
Parameter Sets: (All)
Aliases: 
Accepted values: None, Service, ServiceAndApi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MetricsType
A mérőszám típusát adja meg.
Ez a cmldet az Azure Storage Service metrikák típusát a paraméter által megadott értékre állítja.
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

### -PassThru
Azt jelzi, hogy ez a parancsmag a frissített metrikák tulajdonságot adja eredményül.
Ha nem adja meg ezt a paramétert, ez a parancsmag nem ad vissza értéket.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RetentionDays
Annak a napoknak a száma, ameddig az Azure Storage Service megőrzi a metrikák adatait.

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

### -ServiceType
A tárterület szolgáltatás típusát adja meg.
Ez a parancsmag módosítja a paraméter által megadott szolgáltatási típus metrikájának tulajdonságait.
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

### -Verzió
Az Azure-tárterület metrikájának verziószámát adja meg.
Az alapértelmezett érték a 1,0.

```yaml
Type: Double
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

[Get-AzureStorageServiceMetricsProperty](./Get-AzureStorageServiceMetricsProperty.md)

[Új – AzureStorageContext](./New-AzureStorageContext.md)


