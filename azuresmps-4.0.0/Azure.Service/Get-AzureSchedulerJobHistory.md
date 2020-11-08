---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 2BF5BDF8-3743-46FC-8E04-1A4EA920A2AF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 77b4d184ffbdb1d054f3d14aa3c51c8d2afc928b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016310"
---
# Get-AzureSchedulerJobHistory

## Áttekintés
Meglesz az előzmények egy ütemező feladathoz.

## SZINTAXISA

```
Get-AzureSchedulerJobHistory -Location <String> -JobCollectionName <String> -JobName <String>
 [-JobStatus <String>] [-Profile <AzureSMProfile>] [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>]
 [<CommonParameters>]
```

## Leírás
Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.
A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .

A **Get-AzureSchedulerJobHistory** parancsmag a Scheduler-feladatok előzményeit kapja.

## Példák

### Példa 1: a projekt előzményeinek beolvasása a nevével
```
PS C:\> Get-AzureSchedulerJobHistory -Location "North Central US" -JobCollectionName "JobCollection01" -JobName "Job01"
```

Ez a parancs a Job01 nevű feladat előzményeit kapja.
Ez a feladat a megadott helyen lévő JobCollection01 nevű webhelycsoporthoz tartozik.

### 2. példa: a sikertelen munka előzményeinek beolvasása a neve segítségével
```
PS C:\> Get-AzureSchedulerJobHistory -Location "North Central US" -JobCollectionName "JobCollection01" -JobName "Job12" -JobStatus "Failed"
```

Ez a parancs a Job12 nevű feladat előzményeit kapja meg, amelynek állapota nem sikerült.
Ez a feladat a megadott helyen lévő JobCollection01 nevű webhelycsoporthoz tartozik.

## PARAMÉTEREK

### – Első
Csak a megadott számú objektumot kapja meg.
Adja meg a bejutni kívánt objektumok számát.

```yaml
Type: UInt64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludeTotalCount
A kijelölt objektumok által követett összes objektum (egész) számát adja eredményül.
Ha a parancsmag nem tudja megállapítani a teljes számlálást, az "ismeretlen összeg száma" szöveget jeleníti meg. Az egész számnak van egy pontossági tulajdonsága, amely az összeg megbízhatóságát jelzi.
Az 0,0-től 1,0-ig terjedő pontossági értékek értéke, ahol az 0,0 azt jelenti, hogy a parancsmag nem tudta megszámolni az objektumokat, az 1,0 azt jelenti, hogy a darab pontos, és a 0,0 és a 1,0 közötti érték egyre megbízhatóbb becslést ad.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobCollectionName
A Scheduler-gyűjtemény nevét adja meg.
Ez a parancsmag egy olyan projekt előzményeit kapja meg, amely a paraméter által megadott gyűjteményhez tartozik.

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
Annak a Scheduler-feladatnak a nevét adja meg, amelynek az előzményeit meg szeretné kapni.

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

### -JobStatus
Annak a Scheduler-feladatnak a állapotát adja meg, amelynek az előzményeit meg szeretné kapni.
A paraméter elfogadható értékei a következők:

- Kész
- Sikertelen

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
Az érvényes értékek a következők: 

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

### -Skip (kihagyás)
Figyelmen kívül hagyja a megadott számú objektumot, majd Kinyeri a fennmaradó objektumokat.
Adja meg, hogy hány objektum legyen kihagyva.

```yaml
Type: UInt64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureSchedulerJob](./Get-AzureSchedulerJob.md)

[Get-AzureSchedulerJobCollection](./Get-AzureSchedulerJobCollection.md)


