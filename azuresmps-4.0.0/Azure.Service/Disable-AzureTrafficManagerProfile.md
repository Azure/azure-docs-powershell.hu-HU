---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: ECE9C2A6-7DA2-4477-B877-9970FBE26D7C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8f378cbf8926a650699ec50a2a0a42873dcb7528
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015693"
---
# Disable-AzureTrafficManagerProfile

## Áttekintés
Letiltja a Traffic Manager-profilt.

## SZINTAXISA

```
Disable-AzureTrafficManagerProfile -Name <String> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **disable-AzureTrafficManagerProfile** parancsmag letiltja a Microsoft Azure Traffic Manager-profilt.
A *PassThru* paraméterrel megtekintheti, hogy a művelet sikerül-e.

## Példák

### 1. példa: a Traffic Manager-profil letiltása és az eredmények megjelenítése
```
PS C:\>Disable-AzureTrafficManagerProfile -Name "MyProfile" -PassThru
True
```

Ez a parancs letiltja a MyProfile nevű Traffic Manager-profilt.
A parancs a *PassThru* paramétert adja meg, hogy a parancs sikeres volt-e.

### 2. példa: a forgalomirányító-profil letiltása és találatok megjelenítése
```
PS C:\>Disable-AzureTrafficManagerProfile -Name "MyProfile"
```

Ez a parancs letiltja a MyProfile nevű Traffic Manager profilt, de nem jeleníti meg, hogy a parancs sikerült-e.

## PARAMÉTEREK

### -Name (név)
A letiltani kívánt forgalomirányító-profil nevét adja meg.

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

### -PassThru
Ha a művelet sikeres, akkor az $True értékét számítja ki. egyéb esetben $False.
Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható. Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.

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

### System. Boolean
Ez a parancsmag $True vagy $Falset hoz létre.
Ha a művelet sikeres, és a *PassThru* paramétert adja meg, ez a parancsmag az $True értékét adja eredményül.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Enable-AzureTrafficManagerProfile](./Enable-AzureTrafficManagerProfile.md)

[Get-AzureTrafficManagerProfile](./Get-AzureTrafficManagerProfile.md)

[Új – AzureTrafficManagerProfile](./New-AzureTrafficManagerProfile.md)

[Remove-AzureTrafficManagerProfile](./Remove-AzureTrafficManagerProfile.md)

[Set-AzureTrafficManagerProfile](./Set-AzureTrafficManagerProfile.md)


