---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 95298AFC-B492-4EA6-AFC2-E862D3086AF2
online version: ''
schema: 2.0.0
ms.openlocfilehash: f84b1256d7d911d22a4f1344bdf841943ce87ee7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016116"
---
# Remove-AzureServiceDiagnosticsExtension

## Áttekintés
Eltávolítja a felhőalapú szolgáltatás diagnosztikai bővítményét az összes szerepkörön vagy elnevezett szerepkörökön egy bizonyos terjesztési bővítőhelyen.

## SZINTAXISA

### RemoveByRoles (alapértelmezett)
```
Remove-AzureServiceDiagnosticsExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### RemoveAllRoles
```
Remove-AzureServiceDiagnosticsExtension [[-ServiceName] <String>] [[-Slot] <String>] [-UninstallConfiguration]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## Leírás
A **Remove-AzureServiceDiagnosticsExtension** parancsmag eltávolítja a felhőalapú szolgáltatás diagnosztikai bővítményét az összes szerepkörben vagy elnevezett szerepkörökben egy bizonyos terjesztési bővítőhelyen.

## Példák

### 1. példa: egy szolgáltatás diagnosztikai bővítményének eltávolítása
```
PS C:\> Remove-AzureServiceDiagnosticsExtension -ServiceName $Svc
```

Ez a parancs eltávolítja a meghatározott szerepkör diagnosztikai bővítményét.

### 2. példa: egy szolgáltatás diagnosztikai bővítményének eltávolítása meghatározott szerepkörben
```
PS C:\> Remove-AzureServiceDiagnosticsExtension -ServiceName $Svc -Role "WebRole01"
```

Ez a parancs eltávolítja a meghatározott szerepkör diagnosztikai bővítményét.

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
Azt a választható szerepköröket adja meg, amelyekhez a távoli asztali konfigurációt meg szeretné adni.
Ha nem adja meg ezt a paramétert, a program az összes szerepkör alapértelmezett konfigurációjának megfelelően alkalmazza a távoli asztali konfigurációt.

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
Az érvényes értékek a termelés vagy a megállóhelyek.

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
Azt jelzi, hogy ez a parancsmag eltávolítja a felhőalapú szolgáltatásból az összes RDP-konfigurációt.

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

[Get-AzureServiceDiagnosticsExtension](./Get-AzureServiceDiagnosticsExtension.md)

[Set-AzureServiceDiagnosticsExtension](./Set-AzureServiceDiagnosticsExtension.md)


