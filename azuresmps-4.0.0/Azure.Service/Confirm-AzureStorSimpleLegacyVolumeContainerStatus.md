---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 97AC691F-3835-4CEE-B47E-430BE9962AF9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 26fcee5f6cb669ef49993a009aa76e9c9522b180
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015700"
---
# Confirm-AzureStorSimpleLegacyVolumeContainerStatus

## Áttekintés
Kezdeményezi az áttelepített kötet-tárolók véglegesítését vagy visszagörgetését.

## SZINTAXISA

### MigrateSpecificContainer
```
Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId <String> -MigrationOperation <String>
 -LegacyContainerNames <String[]> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### MigrateAllContainer
```
Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId <String> -MigrationOperation <String> [-All]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **Confirm-AzureStorSimpleLegacyVolumeContainerStatus** parancsmag a régi áttelepítés részeként áttelepített mennyiségi tárolók véglegesítését vagy visszagörgetését kezdeményezi.
A visszagörgetés visszaállítja a készülék eredeti tulajdonjogát.
A véglegesítés a tulajdonost a cél készülékhez rendeli.

## Példák

### Példa 1: véglegesítési művelet kezdeményezése meghatározott mennyiségi tárolón
```
PS C:\>Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -LegacyContainerNames "OneSDKAzureCloud" -MigrationOperation Commit
Please check the commit/discard status using Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus
```

A parancs véglegesítési műveletet kezdeményez a megadott mennyiségi tárolón a megadott örökölt konfiguráció-AZONOSÍTÓhoz.
A művelet állapotának megtekintéséhez használja a **Get-AzureStorSimpleLegacyVolumeContainerStatus** parancsmagot.

### 2. példa: visszagörgetési művelet kezdeményezése adott mennyiségi tárolón
```
PS C:\>Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -LegacyContainerNames "OneSDKAzureCloud" -MigrationOperation Rollback
Please check the commit/discard status using Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus
```

Ez a parancs visszagörgetési műveletet kezdeményezett a megadott kötet-tárolóban a megadott örökölt konfiguráció-AZONOSÍTÓhoz.

### 3. példa: véglegesítési művelet kezdeményezése az összes mennyiségi tárolón
```
PS C:\>Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -MigrationOperation Commit -All
Please check the commit/discard status using Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus
```

Ez a parancs véglegesítési műveletet kezdeményez a megadott örökölt konfigurációs AZONOSÍTÓhoz tartozó összes mennyiségi tárolóban.

### Példa 4: visszagörgetési művelet kezdeményezése az összes mennyiségi tárolón
```
PS C:\>Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -MigrationOperation Rollback -All
Please check the commit/discard status using Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus
```

Ez a parancs a megadott örökölt konfigurációs AZONOSÍTÓhoz tartozó összes mennyiségi tárolóban visszagörgetési műveletet kezdeményez.

## PARAMÉTEREK

### -All (mind)
Azt jelzi, hogy ez a parancsmag visszalépési vagy véglegesítési műveletet kezdeményez az importált konfigurációs fájlban lévő összes mennyiségi tárolóban.

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

### -MigrationOperation
Meghatározza, hogy a parancsmag végrehajt-e egy véglegesítést vagy visszagörgetést.
Az érvényes értékek a következők: véglegesítés és visszagörgetés.

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

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureStorSimpleLegacyVolumeContainerStatus](./Get-AzureStorSimpleLegacyVolumeContainerStatus.md)

[Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus](./Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus.md)

[Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan](./Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan.md)


