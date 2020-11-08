---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: FAEA7859-7E58-4343-AD57-7EFC0D87432E
online version: ''
schema: 2.0.0
ms.openlocfilehash: d2886faacd3e9f7d02a008a056dc2145844f8b30
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015434"
---
# Set-AzureTrafficManagerEndpoint

## Áttekintés
Frissíti egy végpont tulajdonságait a forgalomirányítási profilban.

## SZINTAXISA

```
Set-AzureTrafficManagerEndpoint -DomainName <String> [-Location <String>] [-Type <String>] [-Status <String>]
 [-Weight <Int32>] [-MinChildEndpoints <Int32>] -TrafficManagerProfile <IProfileWithDefinition>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **set-AzureTrafficManagerEndpoint** parancsmag frissíti egy végpont tulajdonságait egy Microsoft Azure Traffic Manager-profilban.
Ha a végpont nem létezik az aktuális profilban, ez a parancsmag hozza létre.
Miután hozzáadta a végpontot, átadja az eredményt a **set-AzureTrafficManagerProfile** parancsmagnak a pipeline operátor használatával.
Ez a parancsmag az Azure-hoz csatlakozik a módosítások mentéséhez.

## Példák

### 1. példa: a végpontok frissítése egy profilhoz
```
PS C:\>$TrafficManagerProfile = Get-AzureTrafficManagerProfile -Name "ContosoProfile"
PS C:\> Set-AzureTrafficManagerEndpoint -TrafficManagerProfile $TrafficManagerProfile -DomainName "ContosoApp02.cloudapp.net" -Status "Enabled" -Type "CloudService" -Weight 2 -Location myLocation | Set-AzureTrafficManagerProfile
```

Az első parancs a **Get-AzureTrafficManagerProfile** parancsmagot használja a ContosoProfile nevű profil beolvasásához, majd a $TrafficManagerProfile változóban tárolja.

A második parancs a $TrafficManagerProfile-on tárolt forgalomirányítási profilban frissíti a végpontot.
A végpont a ContosoApp02.cloudapp.net tartománynév.
A parancs a végpont állapotát, típusát, vastagságát és helyét is megadja.
A parancs a módosított profilt átadja a **set-AzureTrafficManagerProfile** parancsmagnak, amellyel az Azure-hoz kapcsolódhat a módosítások mentéséhez.

## PARAMÉTEREK

### -Tartománynév
A módosítandó végpont tartománynevét adja meg.

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
A lehetséges értékek az Azure-körzetek nevei, az itt látható módon  https://azure.microsoft.com/regions/https://azure.microsoft.com/regions/ .

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

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrafficManagerProfile
Annak a Traffic Manager-profil objektumnak a beállítása, amelynek a végpontját módosítani szeretné.

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

Required: False
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

[Add-AzureTrafficManagerEndpoint](./Add-AzureTrafficManagerEndpoint.md)

[Remove-AzureTrafficManagerEndpoint](./Remove-AzureTrafficManagerEndpoint.md)

[Get-AzureTrafficManagerProfile](./Get-AzureTrafficManagerProfile.md)

[Set-AzureTrafficManagerProfile](./Set-AzureTrafficManagerProfile.md)


