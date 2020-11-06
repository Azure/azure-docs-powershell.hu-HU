---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/enable-azurestoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Enable-AzureStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Enable-AzureStorageDeleteRetentionPolicy.md
ms.openlocfilehash: f8303a9d87a2bd5312732bd01eb3d42bd1e0a285
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493305"
---
# Enable-AzureStorageDeleteRetentionPolicy

## Áttekintés
Engedélyezze az Azure Storage blob szolgáltatás adatmegőrzési házirendjének törlését.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Enable-AzureStorageDeleteRetentionPolicy [-RetentionDays] <Int32> [-PassThru] [-Context <IStorageContext>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
Az **enable-AzureStorageDeleteRetentionPolicy** parancsmag az Azure Storage blob szolgáltatás adatmegőrzési házirendjének törlését teszi lehetővé.

## Példák

### Példa 1: a blob-szolgáltatás adatmegőrzési házirendjének engedélyezése
```
C:\PS>Enable-AzureStorageDeleteRetentionPolicy -RetentionDays 3
```

Ez a parancs engedélyezi a blob-szolgáltatás adatmegőrzési házirendjét, és a törölt blob-adatmegőrzési napokat a 3 értékre állítja.

## PARAMÉTEREK

### -Környezet
Azure Storage Context objektum

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

### -PassThru
DeleteRetentionPolicyProperties megjelenítése

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
Megadja a DeleteRetentionPolicy retenciós napjainak számát.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: Days

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Annak megjelenítése, hogy mi történik, ha a parancsmag fut.
A parancsmag nem fut.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext

## KIMENETEK

### Microsoft. WindowsAzure. Storage. Shared. Protocol. DeleteRetentionPolicyProperties

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

