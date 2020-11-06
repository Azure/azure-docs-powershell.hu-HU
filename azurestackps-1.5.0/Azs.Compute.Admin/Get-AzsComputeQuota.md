---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 30a1bc70b4e704d8dadf864dedf7173476909cf2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491480"
---
# Get-AzsComputeQuota

## Áttekintés
Olyan kvótákat ad eredményül, amelyek meghatározzák az objektumok számítási kvótáit.

## SZINTAXISA

### Lista (alapértelmezett)
```
Get-AzsComputeQuota [-Location <String>] [<CommonParameters>]
```

### Beszerzése
```
Get-AzsComputeQuota [-Name] <String> [-Location <String>] [<CommonParameters>]
```

### ResourceId
```
Get-AzsComputeQuota -ResourceId <String> [<CommonParameters>]
```

## Leírás
A meglévő kvóták listájának beszerzése

## Példák

### --------------------------PÉLDA 1--------------------------
```
Get-AzsComputeQuota -Location 'local'
```

A megadott helyen minden számítási kvóta beszerzése.

### --------------------------PÉLDA 2--------------------------
```
Get-AzsComputeQuota 'Default Quota'
```

Meghatározott számítási kvóta beszerzése

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
A kvóta neve.

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: 1
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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

### ComputeQuotaObject

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

