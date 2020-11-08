---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 06f2d231754fc422115cf800ef66189378e0cd4d
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016905"
---
# Get-AzsDiskMigrationJob

## Áttekintés
A felügyelt áttelepítési feladatok listáját számítja ki.

## SZINTAXISA

### Lista (alapértelmezett)
```
Get-AzsDiskMigrationJob [-Status <String>] [-Location <String>] [<CommonParameters>]
```

### ResourceId
```
Get-AzsDiskMigrationJob -ResourceId <String> [<CommonParameters>]
```

### Beszerzése
```
Get-AzsDiskMigrationJob [-Location <String>] -Name <String> [<CommonParameters>]
```

## Leírás
A lemezvezérlő-áttelepítési feladatok listáját számítja ki.

## Példák

### --------------------------PÉLDA 1--------------------------
```
$migration = Get-AzsDiskMigrationJob -location local -Name "mymigrationName"
```

Adott távtárolású áttelepítési feladat beszerzése.

### --------------------------PÉLDA 2--------------------------
```
$migration = Get-AzsDiskMigrationJob -location local
```

A távtárolású áttelepítési feladatok listáját jeleníti meg a helyi helyen.

## PARAMÉTEREK

### -Hely
Az erőforrás helye.

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
Az áttelepítési feladat GUID-neve.

```yaml
Type: String
Parameter Sets: Get
Aliases: MigrationId

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
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Állapot
A lemezvezérlő-áttelepítési feladat állapotának paraméterei.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

### Microsoft. AzureStack. Management. kiszámítás. admin. models. DiskMigrationJob

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

