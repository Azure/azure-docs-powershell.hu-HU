---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: BB216903-B2BB-4948-AC28-408ED6C768F2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6cae249f99282006ff8636e8d727485a223e2a1d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015899"
---
# New-AzureService

## Áttekintés
Azure-szolgáltatást hoz létre.

## SZINTAXISA

### ParameterSetAffinityGroup (alapértelmezett)
```
New-AzureService [-ServiceName] <String> [-AffinityGroup] <String> [[-Label] <String>]
 [[-Description] <String>] [[-ReverseDnsFqdn] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### ParameterSetLocation
```
New-AzureService [-ServiceName] <String> [-Location] <String> [[-Label] <String>] [[-Description] <String>]
 [[-ReverseDnsFqdn] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Leírás
A **New-AzureService** parancsmag új Azure-szolgáltatást hoz létre a jelenlegi előfizetésben.

## Példák

### Példa 1: szolgáltatás létrehozása
```
PS C:\> New-AzureService -ServiceName "MySvc01" -Label "MyTestService" -Location "South Central US"
```

Ez a parancs létrehoz egy MySvc01 nevű új szolgáltatást a Dél-amerikai Közép-amerikai térségben.

### 2. példa: szolgáltatás létrehozása affinitási csoportban
```
PS C:\> New-AzureService -ServiceName "MySvc01" -AffinityGroup NorthRegion
```

Ez a parancs létrehoz egy MySvc01 nevű új szolgáltatást a NorthRegion affinitás csoport használatával.

## PARAMÉTEREK

### -AffinityGroup
Az előfizetéshez társított affinitási csoportot adja meg.
Ha nem adja meg a *hely* paramétert, az affinitás csoport szükséges.

```yaml
Type: String
Parameter Sets: ParameterSetAffinityGroup
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Leírás
A szolgáltatás leírását adja meg.
A Leírás legfeljebb 1024 karakter hosszú lehet.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
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
A szolgáltatás feliratát adja meg.
Előfordulhat, hogy a címke hossza legfeljebb 100 karakter lehet.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Hely
A szolgáltatás helyét adja meg.
Ha nincs meghatározott affinitási csoport, a hely szükséges.

```yaml
Type: String
Parameter Sets: ParameterSetLocation
Aliases: 

Required: True
Position: 1
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

### -ReverseDnsFqdn
A DNS-név teljes tartománynevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Szolgáltatásnév
Az új szolgáltatás nevét adja meg.
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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureService](./Get-AzureService.md)

[Set-AzureService](./Set-AzureService.md)


