---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4403232b45b2a1e69d6148a118e69ccaf80e4a1e
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840497"
---
# Get-AzsUserSubscription

## Áttekintés
A felhasználói előfizetések listájának beszerzése rendszergazdaként.

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
A felhasználói előfizetések listájának beszerzése rendszergazdaként.

## Példák

### --------------------------PÉLDA 1--------------------------
```
Get-AzsUserSubscription
```

A felhasználói előfizetések listájának beszerzése rendszergazdaként.

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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

### Microsoft. AzureStack. Management. Subscriptions. admin. models. előfizetés

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

