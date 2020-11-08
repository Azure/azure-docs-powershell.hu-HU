---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: B2C7E454-F38F-4139-ADA2-D1C59C03CC50
online version: ''
schema: 2.0.0
ms.openlocfilehash: efa519c380ffa78f44e8ac6edebda284a4ce3cd0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016431"
---
# Set-AzureAffinityGroup

## Áttekintés
Egy affinitási csoport tulajdonságainak módosítása

## SZINTAXISA

```
Set-AzureAffinityGroup [-Name] <String> -Label <String> [-Description <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Leírás
A **set-AzureAffinityGroup** parancsmag az Azure affinitás csoport tulajdonságait módosítja.
Módosíthatja a címkét és a leírást.

## Példák

### Példa 1: affinitás csoport módosítása
```
PS C:\> Set-AzureAffinityGroup -Name "South01" -Label "SouthUSProduction" -Description "Production applications for Southern US locations"
```

Ez a parancs módosítja a South01 nevű affinitási csoport címkéjét, a SouthUSProduction a parancs a leírást is módosítja.

## PARAMÉTEREK

### -Leírás
A affinitás csoport leírását adja meg.
A Leírás legfeljebb 1024 karakter hosszú lehet.

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

### -InformationAction
Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.

A paraméter elfogadható értékei a következők:

- Folytassa
- Mellőzése
- Érdeklődni
- SilentlyContinue
- állj
- Felfüggesztheti

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Egy információs változót ad meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Label (címke)
Az affinitás csoport címkéjét adja meg.
A címke legfeljebb 100 karakter hosszú lehet.

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

### -Name (név)
A parancsmag által módosított affinitási csoport nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
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

[Get-AzureAffinityGroup](./Get-AzureAffinityGroup.md)

[Új – AzureAffinityGroup](./New-AzureAffinityGroup.md)

[Remove-AzureAffinityGroup](./Remove-AzureAffinityGroup.md)


