---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7259C717-250C-454A-B0DF-738B70747FF8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 298633bbc95bfb13ae340dea242c6c04267d479e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015953"
---
# Set-AzureLoadBalancedEndpoint

## Áttekintés
Egy Azure-szolgáltatáson belül a terheléselosztásban beállított összes végpontot módosítja.

## SZINTAXISA

### DefaultProbe (alapértelmezett)
```
Set-AzureLoadBalancedEndpoint -LBSetName <String> [-Protocol <String>] [-LocalPort <Int32>]
 [-PublicPort <Int32>] [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>]
 [-InternalLoadBalancerName <String>] [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>]
 [-VirtualIPName <String>] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### TCPProbe
```
Set-AzureLoadBalancedEndpoint -LBSetName <String> [-Protocol <String>] [-LocalPort <Int32>]
 [-PublicPort <Int32>] [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] [-ProbeProtocolTCP]
 [-ProbePort <Int32>] [-ProbeIntervalInSeconds <Int32>] [-ProbeTimeoutInSeconds <Int32>]
 [-InternalLoadBalancerName <String>] [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>]
 [-VirtualIPName <String>] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### HTTPProbe
```
Set-AzureLoadBalancedEndpoint -LBSetName <String> [-Protocol <String>] [-LocalPort <Int32>]
 [-PublicPort <Int32>] [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] [-ProbeProtocolHTTP]
 -ProbePath <String> [-ProbePort <Int32>] [-ProbeIntervalInSeconds <Int32>] [-ProbeTimeoutInSeconds <Int32>]
 [-InternalLoadBalancerName <String>] [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>]
 [-VirtualIPName <String>] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Leírás
A **set-AzureLoadBalancedEndpoint** parancsmag az Azure-szolgáltatásokban beállított terheléselosztó összes végpontját módosítja.

## Példák

### Példa 1: a terheléselosztási halmazban lévő végpontok módosítása
```
PS C:\> Set-AzureLoadBalancedEndpoint -ServiceName "ContosoService" -LBSetName "LBSet01" -Protocol "TCP" -LocalPort 80 -ProbeProtocolTCP -ProbePort 8080
```

Ez a parancs a LBSet01 nevű terheléselosztó készlet minden végpontját módosítja a TCP-protokoll és a 80-as privát port használata esetén.
A kiegyenlítő szondát beállító parancs a 8080-es porton lévő TCP-protokollt használja.

### 2. példa: adjon meg egy másik virtuális IP-címet.
```
PS C:\> Set-AzureLoadBalancedEndpoint -ServiceName "ContosoService" -LBSetName "LBSet02" -VirtualIPName "Vip01"
```

Ez a parancs módosítja azt a terheléselosztást, amely a terheléselosztó készlet nevében a virtuális IP nevű Vip01.

## PARAMÉTEREK

### -ACL
Olyan hozzáférés-vezérlési lista (ACL) konfigurációs objektumát adja meg, amelyre a parancsmag a végpontokra érvényes.

```yaml
Type: NetworkAclObject
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DirectServerReturn
Annak megadása, hogy a parancsmag engedélyezi-e a közvetlen kiszolgáló visszaadását.
Adja meg az engedélyezni vagy letiltani $True $Falset.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IdleTimeoutInMinutes
A TCP üresjárati időtúllépési időszakát adja meg percben a végpontok esetében.

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

### -InternalLoadBalancerName
Annak a belső terheléselosztó a nevét adja meg, amelyre a parancsmag a konfigurációt tartalmazza.

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

### -LBSetName
Annak a terheléselosztó készletnek a nevét adja meg, amelyet a parancsmag frissít.

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

### -LoadBalancerDistribution
A terheléselosztó terjesztési algoritmusát adja meg.
Az érvényes értékek a következők: 

- sourceIP.
Két rekordos affinitás: Source IP, cél IP 
- sourceIPProtocol.
Három rekordos affinitás: Source IP, cél IP, Protocol 
- nincs.
Öt rekordos affinitás: Source IP, Source port, cél IP, cél port, Protocol 

Az alapértelmezett érték a nincs.

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

### -LocalPort
Itt adhatja meg az adott végpontok által használt helyi, privát portot.
A virtuális gépen futó alkalmazások ebben a portban figyelik ezt a portot a végponthoz tartozó bejelentkezési kérelmekhez.

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

### -ProbeIntervalInSeconds
A végpontok lekérdezési gyakoriságát adja meg másodpercben.

```yaml
Type: Int32
Parameter Sets: TCPProbe, HTTPProbe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProbePath
A HTTP-szonda relatív elérési útvonalát adja meg.

```yaml
Type: String
Parameter Sets: HTTPProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProbePort
A terheléselosztó szondát használó portot adja meg.

```yaml
Type: Int32
Parameter Sets: TCPProbe, HTTPProbe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProbeProtocolHTTP
Megadja, hogy a terheléselosztási végpontok HTTP-szondát használjanak.

```yaml
Type: SwitchParameter
Parameter Sets: HTTPProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProbeProtocolTCP
Azt adja meg, hogy a terheléselosztási végpontok TCP-szondát használjanak.

```yaml
Type: SwitchParameter
Parameter Sets: TCPProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProbeTimeoutInSeconds
A szondával való szavazás időpontját adja meg másodpercben.

```yaml
Type: Int32
Parameter Sets: TCPProbe, HTTPProbe
Aliases: 

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

### -Protocol
A végpontok protokollját adja meg.
Az érvényes értékek a következők: 

- TCP 
- UDP

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

### -PublicPort
A végpont által használt nyilvános portot adja meg.
Ha nem ad meg értéket, az Azure kiosztja az elérhető portot.

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

### -Szolgáltatásnév
Annak az Azure-szolgáltatásnak a neve, amely a parancsmag által módosított végpontokat tartalmazza.

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

### -VirtualIPName
Annak a virtuális IP-címnek a nevét adja meg, amely az Azure-t a végpontokhoz társítja.
Ha virtuális IP-ket szeretne hozzáadni a szolgáltatáshoz, használja az **Add-AzureVirtualIP** parancsmagot.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzureVirtualIP](./Add-AzureVirtualIP.md)

[Set-AzureInternalLoadBalancer](./Set-AzureInternalLoadBalancer.md)


