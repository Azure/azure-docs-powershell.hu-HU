---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 28136DC3-520B-4134-8736-93D86EEABAE1
online version: ''
schema: 2.0.0
ms.openlocfilehash: bf9fd7b67b63ce2bddb762c7006722b6035ffe87
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015536"
---
# Get-AzureTrafficManagerProfile

## Áttekintés
A forgalomirányító-profil részleteit kapja meg.

## SZINTAXISA

```
Get-AzureTrafficManagerProfile [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **Get-AzureTrafficManagerProfile** parancsmag a Microsoft Azure Traffic Manager-profil adatait kapja meg.
Ha nem adja meg a *Name* paramétert, a parancsmag a forgalomirányítási profilokat az aktuális előfizetésben jeleníti meg.

## Példák

### Példa 1: a forgalomirányító-profilok listájának beszerzése az előfizetésben
```
PS C:\>Get-AzureTrafficManagerProfile
```

Ez a parancs beolvassa a forgalomirányító-profilok listáját az előfizetésben.

### 2. példa: adatforgalmi vezető profil beszerzése
```
PS C:\>Get-AzureTrafficManagerProfile -Name "MyProfile"
```

Ez a parancs a MyProfile nevű forgalomirányítási profilt kapja.

### 3. példa: végpont felvétele a forgalomirányító profiljába
```
PS C:\>Get-AzureTrafficManagerProfile -Name "MyProfile" | Add-AzureTrafficManagerEndpoint -DomainName "Myapp2.cloudapp.net" -TrafficManagerProfile $MyTrafficManagerProfile -Type "CloudService" -Status "Enabled" | Set-AzureTrafficManagerProfile
```

A parancs hozzáadja a végpontot egy forgalomirányító-profilhoz, majd menti a profilt.

## PARAMÉTEREK

### -Name (név)
A beolvasott forgalomirányítási profil nevét adja meg.

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

### Microsoft. WindowsAzure. Command. Utilities. TrafficManager. models. IProfileWithDefinition
Ez a parancsmag a forgalomirányító-profil objektumát vagy objektumait hozza létre.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzureTrafficManagerEndpoint](./Add-AzureTrafficManagerEndpoint.md)

[Disable-AzureTrafficManagerProfile](./Disable-AzureTrafficManagerProfile.md)

[Enable-AzureTrafficManagerProfile](./Enable-AzureTrafficManagerProfile.md)

[Új – AzureTrafficManagerProfile](./New-AzureTrafficManagerProfile.md)

[Remove-AzureTrafficManagerProfile](./Remove-AzureTrafficManagerProfile.md)

[Set-AzureTrafficManagerProfile](./Set-AzureTrafficManagerProfile.md)


