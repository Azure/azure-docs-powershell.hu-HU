---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 8FF1362B-C7AB-4769-A88B-D1B6E214A006
online version: ''
schema: 2.0.0
ms.openlocfilehash: cf8275b8dfec4263c5ab7a8022dcb65edccb1171
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016407"
---
# Stop-AzureSiteRecoveryJob

## Áttekintés
Webhely-helyreállítási feladat leállítása.

## SZINTAXISA

### ByObject (alapértelmezett)
```
Stop-AzureSiteRecoveryJob -Job <ASRJob> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ById
```
Stop-AzureSiteRecoveryJob -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **stop-AzureSiteRecoveryJob** parancsmag leállítja az Azure webhely-helyreállítási feladatot.

## Példák

### Példa 1: az összes feladat leállítása
```
PS C:\>$Jobs = Get-AzureSiteRecoveryJob 
PS C:\> Stop-AzureSiteRecoveryJob -Job $Jobs
```

Az első parancs a **Get-AzureSiteRecoveryJob** parancsmag használatával megkapja az Azure webhely-helyreállítási feladatokat az aktuális Azure webhely-helyreállítási tárolóhoz, majd a $Jobs változóban tárolja az eredményeket.

A második parancs leállítja az $Jobs által megadott feladatokat.

## PARAMÉTEREK

### -Azonosító
A leállításhoz adja meg a feladat AZONOSÍTÓját.

```yaml
Type: String
Parameter Sets: ById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Job
A leállítási feladatot adja meg.

```yaml
Type: ASRJob
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

[Get-AzureSiteRecoveryJob](./Get-AzureSiteRecoveryJob.md)

[Újraindítás – AzureSiteRecoveryJob](./Restart-AzureSiteRecoveryJob.md)

[Önéletrajz – AzureSiteRecoveryJob](./Resume-AzureSiteRecoveryJob.md)


