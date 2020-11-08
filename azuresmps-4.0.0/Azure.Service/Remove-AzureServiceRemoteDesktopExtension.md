---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: C263CCAD-E51F-420E-9AD4-4FAC09C99CB1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3c10a7694034fe4400ed415891e74f7089ce8558
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016112"
---
# Remove-AzureServiceRemoteDesktopExtension

## Áttekintés
Eltávolítja a felhőalapú szolgáltatás távoli asztali bővítményét, amelyet az összes szerepkör vagy elnevezett szerepkör a megadott központi telepítő bővítőhelyen alkalmazott.

## SZINTAXISA

### RemoveByRoles (alapértelmezett)
```
Remove-AzureServiceRemoteDesktopExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### RemoveAllRoles
```
Remove-AzureServiceRemoteDesktopExtension [[-ServiceName] <String>] [[-Slot] <String>]
 [-UninstallConfiguration] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Leírás
A **Remove-AzureServiceRemoteDesktopExtension** parancsmag eltávolítja a felhőalapú szolgáltatás távoli asztali bővítményét az összes szerepkörön vagy elnevezett szerepkörökön egy bizonyos központi telepítő bővítőhelyen.

## Példák

### 1. példa: a távoli asztali bővítmény eltávolítása
```
PS C:\> Remove-AzureServiceRemoteDesktopExtension -ServiceName $svc
```

Ez a parancs eltávolítja a távoli asztali bővítményt.

### 2. példa: a távoli asztali bővítmény eltávolítása meghatározott szerepkörről
```
PS C:\> Remove-AzureServiceRemoteDesktopExtension -ServiceName $svc -Role "WebRole1"
```

Ez a parancs eltávolítja a távoli asztali bővítményt egy adott szerepkörből.

## PARAMÉTEREK

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

### -Role (szerepkör)
A szerepkörök választható tömbjét adja meg a távoli asztali konfiguráció megadásához.
Ha nincs megadva, a program az összes szerepkör alapértelmezett konfigurációjának megfelelően alkalmazza a távoli asztali konfigurációt.

```yaml
Type: String[]
Parameter Sets: RemoveByRoles
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Szolgáltatásnév
A központi üzembe helyezés Azure-szolgáltatás nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Slot
A módosítani kívánt központi verzió környezetét adja meg.
A támogatott értékek a "termelés" vagy a "megállóhely".

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UninstallConfiguration
Azt adja meg, hogy a parancsmag eltávolítja a felhőalapú szolgáltatásból az összes RDP-konfigurációt.

```yaml
Type: SwitchParameter
Parameter Sets: RemoveAllRoles
Aliases: 

Required: True
Position: 2
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

[Set-AzureServiceRemoteDesktopExtension](./Set-AzureServiceRemoteDesktopExtension.md)


