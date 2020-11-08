---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 54C89A5F-BF94-468C-92E7-224808FDD0EC
online version: ''
schema: 2.0.0
ms.openlocfilehash: be84995e4826b79befc6282133d70f3ee4a79b4f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016227"
---
# New-AzureAffinityGroup

## Áttekintés
Affinitási csoportot hoz létre a jelenlegi előfizetésben.

## SZINTAXISA

```
New-AzureAffinityGroup [-Name] <String> [-Label <String>] [-Description <String>] -Location <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## Leírás
A **New-AzureAffinityGroup** parancsmag az Azure affinitás csoportot az aktuális Azure-előfizetésből hozza létre.

Az affinitás csoport a szolgáltatásokat és az erőforrásokat egy Azure Datacenter-adatközpontban helyezi el együtt.
Az affinitás csoport tagjai az optimális teljesítmény érdekében csoportosítják a tagokat.
Adjon meg affinitási csoportokat az előfizetési szinten.
Az affinitási csoportok az Ön által létrehozott minden további felhőalapú szolgáltatásban vagy tárolási fiókban elérhetők.
Csak akkor vehet fel szolgáltatásokat az affinitás csoportba, amikor létrehozta.

## Példák

### 1. példa: affinitási csoport létrehozása
```
PS C:\> New-AzureAffinityGroup -Name "South01" -Location "South Central US" -Label "South Region" -Description "Affinity group for production applications in southern region."
```

Ez a parancs létrehoz egy South01 nevű affinitási csoportot a dél-közép-amerikai régióban.
A parancs egy címkét és egy leírást ad meg.

## PARAMÉTEREK

### -Leírás
A affinitás csoport leírását adja meg.
Lehet, hogy a Leírás legfeljebb 1024 karakter hosszú lehet.

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
Előfordulhat, hogy a címke legfeljebb 100 karakter hosszú lehet.

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

### -Hely
Annak az Azure Datacenter-adatközpontnak a földrajzi helyét adja meg, ahol a parancsmag létrehozta az affinitás csoportot.

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
A affinitás csoport nevét adja meg.
A névnek egyedinek kell lennie az előfizetésben.

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

[Remove-AzureAffinityGroup](./Remove-AzureAffinityGroup.md)

[Set-AzureAffinityGroup](./Set-AzureAffinityGroup.md)


