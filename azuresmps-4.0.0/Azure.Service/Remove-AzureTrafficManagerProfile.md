---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: B96A64DD-9005-4B04-A720-6FCF33797E8D
online version: ''
schema: 2.0.0
ms.openlocfilehash: e1fa73aa4e38c8d222da6e73508e9a18a15c1e3f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016091"
---
# Remove-AzureTrafficManagerProfile

## Áttekintés
A forgalomirányító-profil eltávolítása.

## SZINTAXISA

```
Remove-AzureTrafficManagerProfile -Name <String> [-Force] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Leírás
A **Remove-AzureTrafficManagerProfile** parancsmag eltávolítja a Microsoft Azure Traffic Manager-profilt a jelenlegi előfizetésből.

## Példák

### 1. példa: forgalomirányító-profil eltávolítása
```
PS C:\>Remove-AzureTrafficManagerProfile -Name "MyProfile"
```

Ez a parancs eltávolítja a MyProfile nevű Traffic Manager-profilt.

### 2. példa: a Traffic Manager-profil eltávolítása
```
PS C:\>Remove-AzureTrafficManagerProfile -Name "MyProfile" -Force -PassThru
```

Ez a parancs eltávolítja a MyProfile nevű forgalomirányító-profilt, és nem kér megerősítést, és az eredményt visszaszámítja.

## PARAMÉTEREK

### -Force
Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.

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

### -Name (név)
A törlendő forgalomirányítási profil nevét adja meg.

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

[Disable-AzureTrafficManagerProfile](./Disable-AzureTrafficManagerProfile.md)

[Enable-AzureTrafficManagerProfile](./Enable-AzureTrafficManagerProfile.md)

[Get-AzureTrafficManagerProfile](./Get-AzureTrafficManagerProfile.md)

[Új – AzureTrafficManagerProfile](./New-AzureTrafficManagerProfile.md)

[Set-AzureTrafficManagerProfile](./Set-AzureTrafficManagerProfile.md)


