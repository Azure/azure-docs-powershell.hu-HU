---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/disable-azurestoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Disable-AzureStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Disable-AzureStorageDeleteRetentionPolicy.md
ms.openlocfilehash: d3de0cc49eb0e36572daa9e4cfbbb41c0db0936a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672182"
---
# Disable-AzureStorageDeleteRetentionPolicy

## Áttekintés
Tiltsa le a törlés adatmegőrzési házirendet az Azure Storage blob szolgáltatásban.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Disable-AzureStorageDeleteRetentionPolicy [-PassThru] [-Context <IStorageContext>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Leírás
A **disable-AzureStorageDeleteRetentionPolicy** parancsmag letiltja a törlés-adatmegőrzési házirendet az Azure Storage blob szolgáltatáshoz.

## Példák

### 1. példa: a blob-szolgáltatás adatmegőrzési házirendjének letiltása
```
C:\PS>Disable-AzureStorageDeleteRetentionPolicy
```

Ez a parancs letiltja a blob-szolgáltatás adatmegőrzési házirendjének törlését.

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

### Microsoft. WindowsAzure. Command. Storage. Model. resourcemod. PSSeriviceProperties

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

