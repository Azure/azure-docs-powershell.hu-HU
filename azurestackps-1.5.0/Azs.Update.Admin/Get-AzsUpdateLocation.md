---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a9234cb73b1f9c3652827293ae2813f78d7ce336
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491552"
---
# Get-AzsUpdateLocation

## Áttekintés
A frissítési helyek listájának beszerzése

## SZINTAXISA

### Lista (alapértelmezett)
```
Get-AzsUpdateLocation [-ResourceGroupName <String>] [<CommonParameters>]
```

### Beszerzése
```
Get-AzsUpdateLocation [-Name <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### ResourceId
```
Get-AzsUpdateLocation -ResourceId <String> [<CommonParameters>]
```

## Leírás
A frissítési helyek listájának beszerzése A visszaadott helyek használhatók az elérhető frissítések eléréséhez a Get-AzsUpdate segítségével.

## Példák

### --------------------------PÉLDA 1--------------------------
```
Get-AzsUpdateLocation
```

A frissítési helyek listájának beszerzése

## PARAMÉTEREK

### -Name (név)
A frissítési hely neve.

```yaml
Type: String
Parameter Sets: Get
Aliases: Location

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Az az erőforráscsoport, amelyet az erőforrás a csoportban található.

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

### Microsoft. AzureStack. Management. Update. admin. models. UpdateLocation

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

