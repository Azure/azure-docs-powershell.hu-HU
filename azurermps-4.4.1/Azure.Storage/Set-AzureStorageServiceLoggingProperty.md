---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 5422429E-C609-4C1F-A021-E2A085B5F74E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageServiceLoggingProperty.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: baba161c849918c95d5e1df91330dfd96a4c5629
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503339"
---
# Set-AzureStorageServiceLoggingProperty

## Áttekintés
Az Azure Storage Services naplózásának módosítása.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Set-AzureStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Version <Double>]
 [-RetentionDays <Int32>] [-LoggingOperations <LoggingOperations[]>] [-PassThru] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## Leírás
A **set-AzureStorageServiceLoggingProperty** parancsmag az Azure Storage Services naplózását módosítja.

## Példák

### 1. példa: a blob-szolgáltatás naplózási tulajdonságainak módosítása
```
C:\PS>Set-AzureStorageServiceLoggingProperty -ServiceType Blob -LoggingOperations Read,Write -PassThru -RetentionDays 10 -Version 1.0
```

Ez a parancs módosítja a 1,0-ös verzió naplózását a blob-tárolóhoz az olvasási és írási műveletek elvégzéséhez.
Az Azure Storage Service naplózása 10 napra megőrzi a bejegyzéseket.
Mivel a parancs a *PassThru* paramétert adja meg, a parancs a módosított naplózási tulajdonságokat jeleníti meg.

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

### -LoggingOperations
Az Azure Storage Service-műveletek tömbjét adja meg.
Az Azure Storage Services naplózza azokat a műveleteket, amelyeket a paraméter határoz meg.
A paraméter elfogadható értékei a következők:

- Nincs
- Olvasása
- Írni
- Törlése
- Minden

```yaml
Type: LoggingOperations[]
Parameter Sets: (All)
Aliases: 
Accepted values: None, Read, Write, Delete, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Azt jelzi, hogy ez a parancsmag a frissített naplózási tulajdonságokat adja eredményül.
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
Annak a napoknak a száma, ameddig az Azure Storage szolgáltatás megőrzi a naplózási információkat.

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
Ez a parancsmag módosítja a szolgáltatás típusának naplózási tulajdonságait, amelyeket a paraméter határoz meg.
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
Az Azure Storage Service naplózásának verziószámát adja meg.
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

### IStorageContext

A "környezet" paraméter elfogadja a "IStorageContext" típusú értéket a csővezetékről

## KIMENETEK

### Microsoft. WindowsAzure. Storage. Shared. Protocol. LoggingProperties

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureStorageServiceLoggingProperty](./Get-AzureStorageServiceLoggingProperty.md)

[Új – AzureStorageContext](./New-AzureStorageContext.md)


