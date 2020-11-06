---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3ae30d06970d9533c32c96f33a1917fa8d2a6e41
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490800"
---
# Get-AzsDirectoryTenant

## Áttekintés
Felsorolja az összes címtár-bérlői fiókot a jelenlegi előfizetés és a megadott erőforráscsoport nevében.

## SZINTAXISA

### Lista (alapértelmezett)
```
Get-AzsDirectoryTenant [-ResourceGroupName <String>] [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

### Beszerzése
```
Get-AzsDirectoryTenant -Name <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### ResourceId
```
Get-AzsDirectoryTenant -ResourceId <String> [<CommonParameters>]
```

## Leírás
Felsorolja az összes címtár-bérlői fiókot a jelenlegi előfizetés és a megadott erőforráscsoport nevében.

## Példák

### --------------------------PÉLDA 1--------------------------
```
Get-AzsDirectoryTenant -ResourceGroupName "System.Local"
```

Felsorolja az összes címtár-bérlői fiókot a jelenlegi előfizetés és a megadott erőforráscsoport nevében.

## PARAMÉTEREK

### -Name (név)
Címtár-bérlő neve

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
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Skip (kihagyás)
Az első N elem kihagyása a paraméterben megadott értékkel.

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### -Top
A paraméterben megadott módon adja vissza a legfelső N-elemeket.
A-kihagyás paraméter után érvényes.

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

### Microsoft. AzureStack. Management. Subscriptions. admin. models. DirectoryTenant

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

