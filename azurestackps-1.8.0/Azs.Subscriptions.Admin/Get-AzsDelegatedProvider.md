---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: afc99afebed095da96d826918cc6912f197d1899
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93840365"
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
{{Fill DelegatedProviderId Description}}

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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

### Microsoft. AzureStack. Management. Subscriptions. admin. models. előfizetés

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

