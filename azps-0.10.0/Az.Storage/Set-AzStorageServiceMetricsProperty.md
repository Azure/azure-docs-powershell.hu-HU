---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 5878FAD4-A4BB-4DBF-A1F2-221FD34F0308
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageservicemetricsproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Set-AzStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Set-AzStorageServiceMetricsProperty.md
ms.openlocfilehash: 855e7f23c1deddd0e9f0b23e0c04375246e3aa21
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842861"
---
# Set-AzStorageServiceMetricsProperty

## Áttekintés
Módosítja az Azure Storage szolgáltatás metrikák tulajdonságát.

## SZINTAXISA

```
Set-AzStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Version <Double>] [-RetentionDays <Int32>] [-MetricsLevel <MetricsLevel>] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **set-AzStorageServiceMetricsProperty** parancsmag módosítja az Azure Storage szolgáltatás metrikák tulajdonságát.

## Példák

### 1. példa: a blob-szolgáltatás metrikák tulajdonságainak módosítása
```
C:\PS>Set-AzStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour -MetricsLevel Service -PassThru -RetentionDays 10 -Version 1.0
```

Ez a parancs a 1,0-os metrikákat a blob-tárolók számára a szolgáltatás szintjére módosítja.
Az Azure Storage Service metrikája 10 napra megőrzi a bejegyzéseket.
Mivel a parancs a *PassThru* paramétert adja meg, a parancs a módosított metrikák tulajdonságot jeleníti meg.

## PARAMÉTEREK

### -Környezet
Az Azure tárolási környezetét adja meg.
A tárolási környezet eléréséhez használja az New-AzStorageContext parancsmagot.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MetricsLevel
Az Azure-tárterület által a szolgáltatáshoz használt metrikák szintjét adja meg.
A paraméter elfogadható értékei a következők:
- Nincs
- Szolgáltatás
- ServiceAndApi

```yaml
Type: System.Nullable`1[Microsoft.WindowsAz.Storage.Shared.Protocol.MetricsLevel]
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
Type: Microsoft.WindowsAzure.Commands.Storage.Common.ServiceMetricsType
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
Type: System.Management.Automation.SwitchParameter
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
Type: System.Nullable`1[System.Int32]
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
- Fájl: a fájl értéke jelenleg nem támogatott.

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.StorageServiceType
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
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext

## KIMENETEK

### Microsoft. WindowsAz. Storage. Shared. Protocol. MetricsProperties

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzStorageServiceMetricsProperty](./Get-AzStorageServiceMetricsProperty.md)

[Új – AzStorageContext](./New-AzStorageContext.md)


