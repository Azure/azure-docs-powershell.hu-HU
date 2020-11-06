---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 86b9e7574344e1b4724648ce55fa2e36aed6591b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490883"
---
# Get-AzsInfrastructureShare

## Áttekintés
A szövet-fájlmegosztás egy bizonyos helyén lévő listáját számítja ki.

## SZINTAXISA

### Lista (alapértelmezett)
```
Get-AzsInfrastructureShare [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>]
 [<CommonParameters>]
```

### Beszerzése
```
Get-AzsInfrastructureShare [-Name] <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### ResourceId
```
Get-AzsInfrastructureShare -ResourceId <String> [<CommonParameters>]
```

## Leírás
A szövet-fájlmegosztás egy bizonyos helyén lévő listáját számítja ki.

## Példák

### --------------------------PÉLDA 1--------------------------
```
Get-AzsInfrastructureShare
```

Az összes fájlmegosztás listáját számítja ki.

### --------------------------PÉLDA 2--------------------------
```
Get-AzsInfrastructureShare -Name Microsoft.AzureStack.Management.Fabric.Admin.Models.FileShare.Name
```

A név alapján a fájl megosztását adja eredményül.

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
A szövet fájl megosztásának neve.

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

### -ResourceGroupName
Az az erőforráscsoport, amelyben az erőforrás-szolgáltató be van jegyezve.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

### Microsoft. AzureStack. Management. Fabric. admin. models. fájlmegosztásról

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

