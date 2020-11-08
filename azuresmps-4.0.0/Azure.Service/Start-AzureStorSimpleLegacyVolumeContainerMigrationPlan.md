---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 6F31F2B4-6131-4B11-B074-CA05CE3A56F1
online version: ''
schema: 2.0.0
ms.openlocfilehash: f928ecba8f92badc1eb87e47aee16515f1684fce
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015773"
---
# Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan

## Áttekintés
Elindítja az áttelepítési terv létrehozását.

## SZINTAXISA

### MigrateSpecificContainer
```
Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId <String>
 -LegacyContainerNames <String[]> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### MigrateAllContainer
```
Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId <String> [-All]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan** parancsmag az áttelepítési terv létrehozását indítja el.
Az áttelepítési terv létrehozása aszinkron.
Az áttelepítési terv állapotának megtekintéséhez használja a **Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan** parancsmagot.

## Példák

### 1. példa: áttelepítési terv indítása
```
PS C:\>Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -LegacyContainerNames "OneSDKAzureCloud"
Successfully started estimating the Migration Plan. Please check details with Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan
```

Ez a parancs elindítja a OneSDKAzureCloud nevű régi tároló áttelepítési tervének létrehozását.
A parancs a terv állapotára vonatkozó üzenetet ad eredményül, és a **Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan** parancsmagot a naprakész adatokhoz használja.

### 2. példa: az áttelepítési terv elindítása az összes mennyiségi tárolóban
```
PS C:\>Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -All
Successfully started estimating the Migration Plan. Please check details with Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan
```

Ez a parancs elindítja az áttelepítési terv létrehozását az összes örökölt kötet-tároló számára az importált konfigurációs fájlban.

## PARAMÉTEREK

### -All (mind)
Azt jelzi, hogy a parancsmag az importált konfigurációs fájlban az összes mennyiségi tárolóra vonatkozóan elindítja az áttelepítés időpontját.

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
A kötet-tárolók neveinek tömbjét adja meg, amelybe áttelepítési tervet szeretne létrehozni.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs

## KIMENETEK

### Karakterlánc
Ez a parancsmag az áttelepítési terv feladatának állapotát számítja ki, ha az a készüléken sikeresen elindult.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan](./Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan.md)


