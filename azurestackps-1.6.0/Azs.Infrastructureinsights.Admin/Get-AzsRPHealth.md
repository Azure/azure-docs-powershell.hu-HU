---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.InfrastructureInsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7e42278eb4ed402d561399dbd1077f819ef3d2cd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671756"
---
# Get-AzsRPHealth

## Áttekintés
Az egyes szolgáltatások állapotának listáját számítja ki.

## SZINTAXISA

### Lista (alapértelmezett)
```
Get-AzsRPHealth [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### Beszerzése
```
Get-AzsRPHealth [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### ResourceId
```
Get-AzsRPHealth -ResourceId <String> [<CommonParameters>]
```

## Leírás
Az egyes szolgáltatások állapotának listáját számítja ki. A AlertSummary tulajdonság a figyelmeztetés/hibák számát tartalmazza.

## Példák

### --------------------------PÉLDA 1--------------------------
```
Get-AzsRPHealth
```

Az egyes szolgáltatások állapotának listáját számítja ki.

### --------------------------PÉLDA 2--------------------------
```
Get-AzsRPHealth -Name "e56bc7b8-c8b5-4e25-b00c-4f951effb22c"
```

Egy szolgáltatás állapotát számítja ki.

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

### -Hely
A régió neve

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

### -Name (név)
Szolgáltatás állapota név.

```yaml
Type: String
Parameter Sets: Get
Aliases: ServiceHealth

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Erőforráscsoport neve, amely az erőforrás lakik.

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

### Microsoft. AzureStack. Management. InfrastructureInsights. admin. models. ServiceHealth

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

