---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88c19285ee7188dab272eeab7a668f5f5dfe22a4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490676"
---
# Get-AzsDelegatedProvider

## Áttekintés
A delegatedProviders beszerzése

## SZINTAXISA

### Lista (alapértelmezett)
```
Get-AzsDelegatedProvider [<CommonParameters>]
```

### Beszerzése
```
Get-AzsDelegatedProvider [-DelegatedProviderId] <Guid> [<CommonParameters>]
```

## Leírás
A delegatedProviders beszerzése

## Példák

### --------------------------PÉLDA 1--------------------------
```
Get-AzsDelegatedProvider
```

A delegált szolgáltatók listájának beszerzése

### --------------------------PÉLDA 2--------------------------
```
Get-AzsDelegatedProvider -DelegatedProviderId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

A megadott meghatalmazott szolgáltató beszerzése.

## PARAMÉTEREK

### -DelegatedProviderId
DelegatedProvider-azonosító.

```yaml
Type: Guid
Parameter Sets: Get
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

### Microsoft. AzureStack. Management. Subscriptions. admin. models. előfizetés

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

