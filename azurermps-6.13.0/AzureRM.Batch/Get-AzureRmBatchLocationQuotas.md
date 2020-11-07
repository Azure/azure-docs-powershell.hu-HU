---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: A39A415A-B403-48D3-AF80-CF7CFE382577
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurermbatchlocationquotas
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchLocationQuotas.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchLocationQuotas.md
ms.openlocfilehash: dea724c77b0574e8235c58a2a696987c94ca586d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679620"
---
# Get-AzureRmBatchLocationQuotas

## Áttekintés
Az előfizetéshez tartozó kötegelt szolgáltatási kvótákat kapja meg az adott helyen.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Get-AzureRmBatchLocationQuotas [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
A megadott előfizetéshez tartozó kötegelt szolgáltatási kvótákat kapja meg az adott helyen.

## Példák

### Példa 1: a kötegelt szolgáltatás kvótájának beszerzése az előfizetéshez a West US régióban
```
PS C:\>Get-AzureRmBatchLocationQuotas -Location "westus"
          AccountQuota Location
          ------------ --------
          1            westus
```

Ez a parancs az aktuális előfizetéshez tartozó kvótákat kapja meg a Nyugat-amerikai régióban.
A visszatérési érték azt jelzi, hogy ez az előfizetés csak egy köteg fiókot hozhat létre ebben a régióban.

## PARAMÉTEREK

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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

### -Hely
Azt a régiót adja meg, amelyre a parancsmag ellenőrzi a kvótákat.
További információ: Azure Regions ( https://azure.microsoft.com/regions) .

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

## KIMENETEK

### Microsoft.Azure.Commands.BatCH. Modellek. PSBatchLocationQuotas

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
