---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a2b639a09789960393ac26d035a80157069dbaaa
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016689"
---
# Get-AzsDisk

## Áttekintés
Azoknak a felügyelt lemezeknek a listáját adja eredményül, amelyek áttelepíthetők a megadott megosztásban.

## SZINTAXISA

### Lista (alapértelmezett)
```
Get-AzsDisk [-Location <String>] [-Start <Int32>] [-SharePath <String>] [-Count <Int32>]
 [-UserSubscriptionId <String>] [-Status <String>] [<CommonParameters>]
```

### ResourceId
```
Get-AzsDisk -ResourceId <String> [<CommonParameters>]
```

### Beszerzése
```
Get-AzsDisk [-Location <String>] -Name <String> [<CommonParameters>]
```

## Leírás
A lemezek listáját számítja ki.

## Példák

### --------------------------PÉLDA 1--------------------------
```
$disks = Get-AzsDisk -location local
```

A felügyelt lemezek listáját a helyi helyen jeleníti meg.
Alapértelmezés szerint az első 100-lemezek lesznek

### --------------------------PÉLDA 2--------------------------
```
$disk = Get-AzsDisk -location local -name $DiskId
```

Adott távtárolású lemez beszerzése.

## PARAMÉTEREK

### -Count
A visszaadni kívánt lemezek maximális száma.

```yaml
Type: Int32
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
A lemez GUID azonosítója identitásként.

```yaml
Type: String
Parameter Sets: Get
Aliases: DiskId

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

### -MegosztásElérésiÚtja
Annak a forrásnak a megosztása, amelyhez az erőforrás tartozik.

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

### – Első lépések
A lekérdezett lemezek kezdési indexe.

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Állapot
A Disk State paraméterei.

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

### -UserSubscriptionId
Bérlői előfizetés azonosítója, amelyhez az erőforrás tartozik.

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

### Microsoft. AzureStack. Management. számítás. admin. models. Disk

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

