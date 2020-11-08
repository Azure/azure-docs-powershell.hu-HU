---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: CF1FC482-812D-4BAD-BA3A-D88E614A5165
online version: ''
schema: 2.0.0
ms.openlocfilehash: 79f212e83ece1def42c6d8de343a42e087f5181a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016376"
---
# Add-AzureTrafficManagerEndpoint

## Áttekintés
Hozzáad egy végpontot a forgalomirányító profiljához.

## SZINTAXISA

```
Add-AzureTrafficManagerEndpoint -DomainName <String> [-Location <String>] -Type <String> -Status <String>
 [-Weight <Int32>] [-MinChildEndpoints <Int32>] -TrafficManagerProfile <IProfileWithDefinition>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **Add-AzureTrafficManagerEndpoint** parancsmag egy végpontot ad hozzá egy Microsoft Azure Traffic Manager-profilhoz.
Miután hozzáadta a végpontot, átadja az eredményt a **set-AzureTrafficManagerProfile** parancsmagnak a pipeline operátor használatával.
Ez a parancsmag az Azure-hoz csatlakozik a módosítások mentéséhez.

## Példák

### 1. példa: végpont felvétele a profilba
```
PS C:\>$TrafficManagerProfile = Get-AzureTrafficManagerProfile -Name "ContosoProfile"
PS C:\> Add-AzureTrafficManagerEndpoint -TrafficManagerProfile $TrafficManagerProfile -DomainName "Contoso02App.cloudapp.net" -Status "Enabled" -Type "CloudService" | Set-AzureTrafficManagerProfile
```

Az első parancs a **Get-AzureTrafficManagerProfile** parancsmagot használja a ContosoProfile nevű profil beolvasásához, majd a $TrafficManagerProfile változóban tárolja.

A második parancs a $TrafficManagerProfile-on tárolt Traffic Manager-profilhoz ad hozzá egy végpontot.
A végpont a Contoso02App.couldapp.net tartománynév.
A parancs azt is megadhatja, hogy engedélyezve van-e a típusa.
A parancs átadja a profil objektumnak a **set-AzureTrafficManagerProfile** parancsmagot az Azure-hoz való csatlakozáshoz a módosítások mentéséhez.

### 2. példa: meghatározott helyet és vastagságot tartalmazó végpont felvétele
```
PS C:\>Add-AzureTrafficManagerEndpoint -TrafficManagerProfile ContosoTrafficManagerProfile -DomainName " Contoso02App.cloudapp.net" -Status Enabled -Type CloudService -Weight 2 -Location myLocation | Set-AzureTrafficManagerProfile
```

Ez a parancs egy végpontot ad a forgalomirányító-profilhoz.
A végpont a Contoso02App.couldapp.net tartománynév.
A parancs azt is megadhatja, hogy engedélyezve van-e a típusa.
A parancs a végpont vastagságát és helyét is megadja.
A parancs átadja a AzureTrafficManagerProfile az Azure **-** hoz való csatlakozáshoz a módosítások mentéséhez.

## PARAMÉTEREK

### -Tartománynév
A hozzáadni kívánt végpont tartománynevét adja meg.

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

### -Hely
A parancsmag által hozzáadott végpont helyét adja meg.
Ehhez az Azure-helynek kell lennie.

Ennek a paraméternek tartalmaznia kell egy, az "any" vagy a "TrafficManager" típusú végpontok értékét egy olyan profilban, amelyben a "teljesítmény" értékre van állítva a terheléselosztási módszer.
A lehetséges értékek az Azure-körzetek nevei, az itt látható módon https://azure.microsoft.com/regions/ .

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

### -MinChildEndpoints
A végpontok minimális számának meghatározása: a beágyazott profilnak online kell lennie ahhoz, hogy a végpont online állapotú legyen.

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

### -Állapot
A figyelési végpont állapotát adja meg.
Az érvényes értékek a következők: 

- Engedélyezve
- Tiltva

Ha megadja az engedélyezett értéket, a Traffic Manager figyeli a végpontot, és a terheléselosztási módszer a forgalom kezelésekor tartja a betöltést.

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

### -TrafficManagerProfile
Annak a Traffic Manager-profil objektumnak a megadása, amelyhez hozzá szeretné adni a végpontot.

```yaml
Type: IProfileWithDefinition
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Type (típus)
A végpont típusát adja meg.
Az érvényes értékek a következők: 

- CloudService
- AzureWebsite
- TrafficManager

- Bármely 

Ha egynél több AzureWebsite-végpont van, a végpontoknak különböző adatközpontokban kell lenniük.

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

### -Weight (súly)
A parancsmag által hozzáadott végpont vastagságát adja meg.
A paraméterhez tartozó érvényes értéktartomány \[ 1, 1000 \] .

Ez a paraméter csak a RoundRobin terheléselosztási házirendek esetében használatos.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

### Microsoft. WindowsAzure. Command. Utilities. TrafficManager. models. IProfileWithDefinition
Ez a parancsmag a Traffic Manager profil objektumát hozza létre, amely a frissített profillal kapcsolatos információkat tartalmazza.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Remove-AzureTrafficManagerEndpoint](./Remove-AzureTrafficManagerEndpoint.md)

[Set-AzureTrafficManagerEndpoint](./Set-AzureTrafficManagerEndpoint.md)

[Get-AzureTrafficManagerProfile](./Get-AzureTrafficManagerProfile.md)

[Set-AzureTrafficManagerProfile](./Set-AzureTrafficManagerProfile.md)


