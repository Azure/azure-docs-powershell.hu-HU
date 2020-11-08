---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 23272A36-8F55-41A8-AFC9-2EEE0FA55DA3
online version: ''
schema: 2.0.0
ms.openlocfilehash: bd341437019b6adbe6c2a5a93076baff61e1f0d7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016258"
---
# Import-AzureStorSimpleLegacyVolumeContainer

## Áttekintés
Elindítja a kötet-tárolók áttelepítését.

## SZINTAXISA

### MigrateSpecificContainer
```
Import-AzureStorSimpleLegacyVolumeContainer -LegacyConfigId <String> -LegacyContainerNames <String[]>
 [-SkipACRs] [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### MigrateAllContainer
```
Import-AzureStorSimpleLegacyVolumeContainer -LegacyConfigId <String> [-All] [-SkipACRs] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
Az **import-AzureStorSimpleLegacyVolumeContainer** parancsmag a kötet-tárolók áttelepítését egy régi készülékről a cél készülékre indítja.

## Példák

### 1. példa: örökölt kötet-tároló importálása
```
PS C:\>Import-AzureStorSimpleLegacyVolumeContainer -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -LegacyContainerNames "OneSDKAzureCloud"
Import started, Please check status with Get-AzureStorSimpleLegacyVolumeContainerStatus commandlet
```

A parancs a megnevezett tároló örökölt kötet tárolóját importálja.
A parancsmag elindítja az importálást, majd egy üzenetet ad eredményül.

### 2. példa: az összes régi mennyiségi tároló importálása
```
PS C:\>Import-AzureStorSimpleLegacyVolumeContainer -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -All
Import started, Please check status with Get-AzureStorSimpleLegacyVolumeContainerStatus commandlet
```

Ezzel a paranccsal importálhatja az összes örökölt mennyiségi tárolót a konfigurációs fájlból.
A parancsmag elindítja az importálást, majd egy üzenetet ad eredményül.

## PARAMÉTEREK

### -All (mind)
Jelzi, hogy ez a parancsmag az importált konfigurációs fájlban lévő összes mennyiségi tárolót importálja a céleszköz.

```yaml
Type: SwitchParameter
Parameter Sets: MigrateAllContainer
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Jelzi, hogy ez a parancsmag mennyiségi tárolót importál egy másik eszközre, még akkor is, ha a kötet tárolóját egy másik eszközön importálta.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LegacyConfigId
A régi készülék konfigurációjának egyedi AZONOSÍTÓját adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LegacyContainerNames
Az áttelepítési terv által érintett mennyiségi tárolók neveinek tömbjét adja meg.

```yaml
Type: String[]
Parameter Sets: MigrateSpecificContainer
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.
Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkipACRs
Jelzi, hogy az importálási folyamat kihagyja a hozzáférés-vezérlési rekordokat az áttelepítéshez.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

### Karakterlánc
Ez a parancs az áttelepítési mennyiség tárolójának állapotát jeleníti meg, ha az sikeresen elindult a készüléken.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureStorSimpleLegacyVolumeContainerStatus](./Get-AzureStorSimpleLegacyVolumeContainerStatus.md)

[Importálás – AzureStorSimpleLegacyApplianceConfig](./Import-AzureStorSimpleLegacyApplianceConfig.md)


