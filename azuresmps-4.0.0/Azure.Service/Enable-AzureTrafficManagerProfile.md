---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 51A1B699-03F6-4BB9-9186-FDFFB094F16A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 72420272e04519fa888660f8ccb6d432ecb0ee5d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016375"
---
# Enable-AzureTrafficManagerProfile

## Áttekintés
Lehetővé teszi a forgalomirányítási profilok betöltését.

## SZINTAXISA

```
Enable-AzureTrafficManagerProfile -Name <String> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
Az **enable-AzureTrafficManagerProfile** parancsmag lehetővé teszi a Microsoft Azure Traffic Manager-profil használatát.
Adja meg a *PassThru* paramétert annak megjelenítéséhez, hogy a művelet sikerül-e.

## Példák

### 1. példa: forgalomirányító-profil engedélyezése
```
PS C:\>Enable-AzureTrafficManagerProfile -Name "MyProfile"
```

Ez a parancs engedélyezi a MyProfile nevű Traffic Manager-profilt.

### 2. példa: a forgalomirányítási profil engedélyezése és a találatok megjelenítése
```
PS C:\>Enable-AzureTrafficManagerProfile -Name "MyProfile" -PassThru
True
```

Ez a parancs engedélyezi a MyProfile nevű Traffic Manager-profilt, és megjeleníti, hogy a parancs sikerült-e.

## PARAMÉTEREK

### -Name (név)
Az engedélyezni kívánt forgalomirányító-profil nevét adja meg.

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
Ha a művelet sikeres, és a *PassThru* paraméter megadása esetén a parancsmag az $True értékét adja eredményül.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Disable-AzureTrafficManagerProfile](./Disable-AzureTrafficManagerProfile.md)

[Get-AzureTrafficManagerProfile](./Get-AzureTrafficManagerProfile.md)

[Új – AzureTrafficManagerProfile](./New-AzureTrafficManagerProfile.md)

[Remove-AzureTrafficManagerProfile](./Remove-AzureTrafficManagerProfile.md)

[Set-AzureTrafficManagerProfile](./Set-AzureTrafficManagerProfile.md)


