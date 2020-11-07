---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 494291A1-D854-4E97-B5EE-27BB5653D97C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceLoggingProperty.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: a3981ba2b0759afec06bb4cf34bc1e086658765a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672084"
---
# Get-AzureStorageServiceLoggingProperty

## Áttekintés
Az Azure Storage Services naplózási tulajdonságait kapja.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

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

### IStorageContext

A "környezet" paraméter elfogadja a "IStorageContext" típusú értéket a csővezetékről

## KIMENETEK

### Microsoft. WindowsAzure. Storage. Shared. Protocol. LoggingProperties

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzureStorageContext](./New-AzureStorageContext.md)

[Set-AzureStorageServiceLoggingProperty](./Set-AzureStorageServiceLoggingProperty.md)


