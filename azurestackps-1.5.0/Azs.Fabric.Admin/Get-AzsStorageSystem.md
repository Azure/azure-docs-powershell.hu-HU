---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 362eb6a8d688aab2276fa1166f65474dab488952
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490900"
---
# Get-AzsStorageSystem

## Áttekintés
A hely összes tárolási alrendszerének listáját jeleníti meg.

## SZINTAXISA

### Lista (alapértelmezett)
```
Get-AzsStorageSystem [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### Beszerzése
```
Get-AzsStorageSystem [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### ResourceId
```
Get-AzsStorageSystem -ResourceId <String> [<CommonParameters>]
```

## Leírás
A hely összes tárolási alrendszerének listáját jeleníti meg.

## Példák

### --------------------------PÉLDA 1--------------------------
```
Get-AzsStorageSystem
```

A tárolási alrendszerek beszerzése egy helyről.

### --------------------------PÉLDA 2--------------------------
```
Get-AzsStorageSystem -Name S-Cluster.azurestack.local
```

A tárolási alrendszer helyét és nevét adja meg.

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
Az az erőforráscsoport, amelyben az erőforrás-szolgáltató be van jegyezve.

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

### Microsoft. AzureStack. Management. Fabric. admin. models. StorageSystem

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

