---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 700AC44E-4FD5-4516-80F3-B8C9E4DF6ABC
online version: ''
schema: 2.0.0
ms.openlocfilehash: d37397b4e0ce9f1d9878860eb5e7a431e58a20a9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015794"
---
# Set-AzureTrafficManagerProfile

## Áttekintés
Frissíti a forgalomirányító-profilok tulajdonságait.

## SZINTAXISA

```
Set-AzureTrafficManagerProfile [-Name <String>] [-LoadBalancingMethod <String>] [-MonitorPort <Int32>]
 [-MonitorProtocol <String>] [-MonitorRelativePath <String>] [-Ttl <Int32>]
 -TrafficManagerProfile <IProfileWithDefinition> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **set-AzureTrafficManagerProfile** parancsmag frissíti a Microsoft Azure Traffic Manager-profilok tulajdonságait.

Azoknál a profiloknál, amelyeknél a *LoadBalancingMethod* értékét a "feladatátvétel" értékre állította, a Add-AzureTrafficManagerEndpoint parancsmaggal meghatározhatja a profiljához hozzáadott végpontok feladatátvételi sorrendjét.
További információért lásd alább a 3.

## Példák

### Példa 1: a forgalomirányító-profil TTL-beállítása
```
PS C:\>Set-AzureTrafficManagerProfile -TrafficManagerProfile $MyTrafficManagerProfile -Ttl 60
```

Ez a parancs a forgalmi vezető profil objektum MyTrafficManagerProfile a TTL (élettartam) értéket 60 másodpercre állítja.

### 2. példa: több érték beállítása egy profilhoz
```
PS C:\>Get-AzureTrafficManagerProfile -Name "MyProfile" | Set-AzureTrafficManagerProfile -LoadBalancingMethod "RoundRobin" -Ttl 30 -MonitorProtocol "Http" -MonitorPort 80 -MonitorRelativePath "/"
```

Ez a parancs a **Get-AzureTrafficManagerProfile** parancsmaggal kapja meg a MyProfile nevű Traffic Manager-profilt.
A profil a RoundRobin-terheléselosztási módszert, a 30 másodperces ÉLETTARTAMot, a monitor Protocol HTTP-t, a monitor portot és a forgalomirányító-profil relatív elérési útját használja.

### 3. példa: a végpontok átrendezése a kívánt feladatátvételi sorrendbe
```
PS C:\>$Profile = Get-AzureTrafficManagerProfile -Name "MyProfile"
PS C:\> $Profile.Endpoints[0],$Profile.Endpoints[1] = $Profile.Endpoints[1],$Profile.Endpoints[0]
PS C:\> $Profile = Set-AzureTrafficManagerProfile
```

Ebben a példában átrendezi a MyProfile hozzáadott végpontokat a kívánt feladatátvételi sorrendbe.

Az első parancs beolvassa a Traffic Manager profil objektum MyProfile nevű objektumát, és a $Profile változóban tárolja az objektumot.

A második parancs átrendezi a végpontokat a végpontok tömbből arra a sorrendre, amelyben a feladatátvételt meg szeretné adni.

Az utolsó parancs frissíti a $Profileban tárolt forgalomirányítási profilt az új végponti sorrendben.

## PARAMÉTEREK

### -LoadBalancingMethod
A kapcsolat elosztásához használt terheléselosztási módszert adja meg.
Az érvényes értékek a következők: 

- Teljesítmény
- Feladatátvétel
- RoundRobin

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

### -MonitorPort
A végpontok állapotának figyeléséhez használt portot adja meg.
Az érvényes értékek a 0 és kisebb, mint 65 535-nél nagyobb egész számok.

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

### -MonitorProtocol
A végpontok állapotának figyeléséhez használható protokollt adja meg.
Az érvényes értékek a következők: 

- Http
- Https

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

### -MonitorRelativePath
A végponthoz viszonyított elérési utat adja meg a szonda állapotához
Az elérési útnak az alábbi korlátozásoknak kell megfelelnie: 

- Az elérési útnak 1-től 1000 karakterből kell állnia.
- Meg kell kezdődnie egy perjelet,/.
- Tartalmaznia kell az XML-elemeket \<\> .
- Nem tartalmazhat dupla ferdeség,//.
- Nem tartalmazhat érvénytelen HTML-Escape-karaktereket.
Például:% XY.

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

### -Name (név)
A frissítendő forgalomirányítási profil nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -TrafficManagerProfile
A Traffic Manager profil objektumát adja meg a profil beállításához.

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

### -TTL (TTL)
Azt a DNS-élettartamot adja meg, amely a helyi DNS-megoldókat a DNS-rekordok gyorsítótárazását követően adja meg.
Az érvényes értékek a 30 és a 999 999 közötti egész számok.

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
Ez a parancsmag a Traffic Manager profil objektumát hozza létre.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Disable-AzureTrafficManagerProfile](./Disable-AzureTrafficManagerProfile.md)

[Enable-AzureTrafficManagerProfile](./Enable-AzureTrafficManagerProfile.md)

[Get-AzureTrafficManagerProfile](./Get-AzureTrafficManagerProfile.md)

[Új – AzureTrafficManagerProfile](./New-AzureTrafficManagerProfile.md)

[Remove-AzureTrafficManagerProfile](./Remove-AzureTrafficManagerProfile.md)


