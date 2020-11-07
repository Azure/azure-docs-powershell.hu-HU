---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5ff90957a655837dbdf75ce3f4242222615f2a73
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93840082"
---
# Get-AzsUserSubscription

## Áttekintés
A felhasználói előfizetések listájának beszerzése operátorként.

## SZINTAXISA

### Lista (alapértelmezett)
```
Get-AzsUserSubscription [-Filter <String>] [<CommonParameters>]
```

### Beszerzése
```
Get-AzsUserSubscription -SubscriptionId <Guid> [<CommonParameters>]
```

## Leírás
A felhasználói előfizetések listájának beszerzése operátorként.

## Példák

### --------------------------PÉLDA 1--------------------------
```
Get-AzsUserSubscription
```

A felhasználói előfizetések listájának beszerzése operátorként.

## PARAMÉTEREK

### -Szűrő
OData-szűrő paraméter

```yaml
Type: String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Előfizetés azonosítója paraméter

```yaml
Type: Guid
Parameter Sets: Get
Aliases:

Required: True
Position: Named
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

