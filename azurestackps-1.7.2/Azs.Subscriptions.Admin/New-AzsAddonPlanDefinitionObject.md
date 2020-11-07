---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 57d7037f6deb669531bb03c3bf4f2e504586f832
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838337"
---
# New-AzsAddonPlanDefinitionObject

## Áttekintés
Annak a kívánt csomagnak a nevét tartalmazza, amelyet fel szeretne venni az ajánlatból, vagy le szeretne kapcsolni.

## SZINTAXISA

```
New-AzsAddonPlanDefinitionObject [[-PlanId] <String>] [[-MaxAcquisitionCount] <Int64>] [<CommonParameters>]
```

## Leírás
Annak a kívánt csomagnak a nevét tartalmazza, amelyet fel szeretne venni az ajánlatból, vagy le szeretne kapcsolni.

## Példák

### --------------------------PÉLDA 1--------------------------
```
New-AzsAddonPlanDefinitionObject -PlanId $planIdentifier -MaxAcquisitionCount 500
```

Új terv-definíciós objektum létrehozása a megadott tervhez az 500 beszerzési korlátozásával.

## PARAMÉTEREK

### -MaxAcquisitionCount
Egyetlen előfizetéssel megszerezhető példányok maximális száma
Ha nincs megadva, a feltételezett érték 1.

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PlanId
Terv azonosítója

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
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

