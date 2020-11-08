---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3874c581d1d030f9c0b77abe82b5a5a289d8960d
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016984"
---
# Get-AzsSubscriptionsQuota

## Áttekintés
Lekérheti az előfizetéses erőforrás-szolgáltatói kvóták listáját egy helyen.

## SZINTAXISA

### Lista (alapértelmezett)
```
Get-AzsSubscriptionsQuota [-Location <String>] [<CommonParameters>]
```

### Beszerzése
```
Get-AzsSubscriptionsQuota -Name <String> [-Location <String>] [<CommonParameters>]
```

### ResourceId
```
Get-AzsSubscriptionsQuota -ResourceId <String> [<CommonParameters>]
```

## Leírás
Letölthet egy helyet a kvóták listájáról.

## Példák

### --------------------------PÉLDA 1--------------------------
```
Get-AzsSubscriptionsQuota
```

Lekérheti az előfizetéses erőforrás-szolgáltatói kvóták listáját egy helyen.

## PARAMÉTEREK

### -Hely
A AzureStack helye.

```yaml
Type: String
Parameter Sets: List, Get
Aliases: ArmLocation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (név)
A kvóta neve.

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Az erőforrás-azonosító.

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

### Microsoft. AzureStack. Management. Subscriptions. admin. modellek. kvóta

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

