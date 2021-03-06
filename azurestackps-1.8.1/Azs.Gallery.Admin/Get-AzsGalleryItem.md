---
external help file: Azs.Gallery.Admin-help.xml
Module Name: Azs.Gallery.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0fa95e34c6a220a496a79f7a72c65c222f1376f1
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840877"
---
# Get-AzsGalleryItem

## Áttekintés
A gyűjtemény felsorolja a gyűjtemény elemeit.

## SZINTAXISA

### Lista (alapértelmezett)
```
Get-AzsGalleryItem [<CommonParameters>]
```

### Beszerzése
```
Get-AzsGalleryItem [-Name] <String> [<CommonParameters>]
```

## Leírás
Az Azure halom piactéren elérhető gyűjtemény-elemek listájának beszerzése

## Példák

### PÉLDA 1
```
Get-AzsGalleryItem
```

A lista gyűjtemény elemei.

### 2. PÉLDA
```
Get-AzsGalleryItem -Name 'microsoft.vmss.1.3.6'
```

Gyűjtemény-elem beszerzése név alapján

## PARAMÉTEREK

### -Name (név)
A gyűjtemény elemeinek azonosítása
Tartalmazza a közzétevő nevét, az elem nevét, valamint tartalmazhat az időszak karakterrel elválasztott verziót.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

### Microsoft. AzureStack. Management. Gallery. admin. models. GalleryItem

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
