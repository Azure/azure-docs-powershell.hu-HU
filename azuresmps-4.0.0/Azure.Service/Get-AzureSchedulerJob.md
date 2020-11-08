---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 8EED9813-5106-4D6C-B869-97BCBD7845AC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 67e354616161ad7f2d2467a37b92c355c7c8c39e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016311"
---
# Get-AzureSchedulerJob

## Áttekintés
A Scheduler-feladatok listáját vagy egy adott ütemező feladatot kapja meg.

## SZINTAXISA

```
Get-AzureSchedulerJob -Location <String> -JobCollectionName <String> [-JobName <String>] [-JobState <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.
A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .

A **Get-AzureSchedulerJobCollection** parancsmag a Scheduler-feladatok listáját, vagy egy adott ütemező feladatot kap.

## Példák

### Példa 1: a gyűjtemény összes feladatának beszerzése
```
PS C:\> Get-AzureSchedulerJob -Location "North Central US" -JobCollectionName "JobCollection01"
```

Ez a parancs a JobCollection01 nevű begyűjtő feladatok részét képezi a Feladatütemezőben.

### 2. példa: elnevezett feladat beszerzése
```
PS C:\> Get-AzureSchedulerJob -Location "North Central US" -JobCollectionName "JobCollection01" -JobName "Job01"
```

Ez a parancs a Job01 nevű feladatot a megadott helyen lévő JobCollection01 nevű gyűjteményből kapja.

### 3. példa: letiltott feladatok lekérése egy gyűjteményben
```
PS C:\> Get-AzureSchedulerJobCollection -Location "North Central US" -JobCollectionName "JobCollection01" -JobState "Disabled"
```

Ez a parancs a megadott helyen található JobCollection01 részét képező, letiltott Scheduler-feladatokat kapja meg.

## PARAMÉTEREK

### -JobCollectionName
Annak a gyűjteménynek a nevét adja meg, amely a beolvasás ütemező feladatát tartalmazza.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Feladatnév
A beolvasott ütemező feladatának nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -JobState
A beolvasott ütemező-feladatok állapotát adja meg.
A paraméter elfogadható értékei a következők:

- Engedélyezve
- Tiltva
- Hibázott
- Kész

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Hely
Annak a helynek a nevét adja meg, amely a felhőalapú szolgáltatást tárolja.
A paraméter elfogadható értékei a következők:

- Bárhonnan Ázsia
- Bárhol Európában
- Bárhol vagyunk
- Kelet-ázsiai
- Kelet-amerikai
- Közép-amerikai Észak-amerikai
- Észak-Európa
- Dél-Közép-amerikai
- Dél-ázsiai
- Nyugat-Európa
- Nyugat-amerikai

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

[Remove-AzureSchedulerJob](./Remove-AzureSchedulerJob.md)


