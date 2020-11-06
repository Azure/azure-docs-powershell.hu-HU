---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 500a8e28ceb4eb452d788574b8a80865b5e54b14
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491503"
---
# Get-AzsBackupConfiguration

## Áttekintés
A biztonságimásolat-konfigurációk listáját számítja ki.

## SZINTAXISA

### Lista (alapértelmezett)
```
Get-AzsBackupConfiguration [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### Beszerzése
```
Get-AzsBackupConfiguration [[-Location] <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### ResourceId
```
Get-AzsBackupConfiguration -ResourceId <String> [<CommonParameters>]
```

## Leírás
A biztonságimásolat-konfigurációk listáját számítja ki.

## Példák

### --------------------------PÉLDA 1--------------------------
```
Get-AzsBackupConfiguration
```

Azure-halom biztonsági mentése konfigurációjának beszerzése

## PARAMÉTEREK

### -Hely
Biztonsági mentési hely

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Az erőforráscsoport neve.

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

### Microsoft. AzureStack. Management. backup. admin. models. BackupLocation

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

