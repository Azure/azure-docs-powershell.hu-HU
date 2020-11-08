---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: DF12406D-894C-4732-95EE-D75524023B82
online version: ''
schema: 2.0.0
ms.openlocfilehash: c2e6596c0de702175927f51bfd70fc5271b13bfd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015980"
---
# New-AzureSchedulerJobCollection

## Áttekintés
Ütemező begyűjtési feladatot hoz létre.

## SZINTAXISA

```
New-AzureSchedulerJobCollection -Location <String> -JobCollectionName <String> [-Plan <String>]
 [-MaxJobCount <Int32>] [-Frequency <String>] [-Interval <Int32>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Leírás
Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.
A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .

A **New-AzureSchedulerJobCollection** parancsmag létrehoz egy Scheduler Job Collectiont.
Ha nem ad meg értéket a *terv* paraméterhez, a parancsmag létrehoz egy szabványos begyűjtő feladatot.

## Példák

### Példa 1: alapértelmezett értékeket tartalmazó Scheduler-gyűjtemény létrehozása
```
PS C:\> New-AzureSchedulerJobCollection -JobCollectionName "JobCollection01" -Location "North Central US" -Plan "Standard"
```

Ez a parancs létrehoz egy JobCollection01 nevű normál Scheduler-munkagyűjteményt.
Az új gyűjteményhez tartozik egy alapértelmezett tevékenység száma és a maximális ismétlődési értékek a szokásos ütemező-összegyűjtéshez.

### 2. példa: a Scheduler-munkagyűjtemény létrehozása megadott értékekkel
```
PS C:\> New-AzureSchedulerJobCollection -JobCollectionName "JobCollection02" -Location "North Central US" -Frequency "Hour" -Interval 12 -MaxJobCount 30 -Plan "Standard"
```

Ez a parancs létrehoz egy JobCollection02 nevű normál Scheduler-munkagyűjteményt.
Az új gyűjteményben a maximális mennyiség 30, a maximálisan 12 óránként

## PARAMÉTEREK

### -Gyakoriság
A Feladatütemezőben a munkafolyamatban bármely feladatban megadható maximális frekvenciát adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Intervallum
A *gyakoriság* paraméterrel megadott gyakoriságú ismétlődési intervallumot adja meg.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobCollectionName
Az új ütemező-beosztáshoz tartozó nevet adja meg.

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
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxJobCount
A Feladatütemezőben létrehozható feladatok maximális számát adja meg.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Terv
A Scheduler Job Collection Plant adja meg.

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

[Get-AzureSchedulerJobCollection](./Get-AzureSchedulerJobCollection.md)

[Remove-AzureSchedulerJobCollection](./Remove-AzureSchedulerJobCollection.md)

[Set-AzureSchedulerJobCollection](./Set-AzureSchedulerJobCollection.md)


