---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 70d8ded2b2954746a97d6144f33c043c27341da4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671708"
---
# New-AzsScaleUnitNodeObject

## Áttekintés
Olyan bemeneti adatok, amelyek lehetővé teszik a méretarányos csomópont hozzáadását.

## SZINTAXISA

```
New-AzsScaleUnitNodeObject [[-BMCIPv4Address] <String>] [[-ComputerName] <String>] [<CommonParameters>]
```

## Leírás
Olyan bemeneti adatok, amelyek lehetővé teszik a méretarányos csomópont hozzáadását.

## Példák

### --------------------------PÉLDA 1--------------------------
```
New-AzsScaleUnitNodeObject -BMCIPv4Address 192.168.1.1 -ComputeName 'NodeName'
```

Új csomópont-objektum létrehozása

## PARAMÉTEREK

### -BMCIPv4Address
A fizikai gép bmc-címe.

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

### -Számítógépnév
A fizikai gép számítógépnevét.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
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

