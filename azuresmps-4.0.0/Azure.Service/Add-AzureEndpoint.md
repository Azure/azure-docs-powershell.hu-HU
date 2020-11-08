---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D767F017-6545-4BC6-927E-E7A99A08D5D2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5b3122795f2af33a28206936b7b28322ad171b19
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015733"
---
# Add-AzureEndpoint

## Áttekintés
Végpontot ad hozzá egy virtuális géphez.

## SZINTAXISA

### NoLB (alapértelmezett)
```
Add-AzureEndpoint [-Name] <String> [-Protocol] <String> [-LocalPort] <Int32> [-PublicPort <Int32>]
 [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] [-InternalLoadBalancerName <String>]
 [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>] [-VirtualIPName <String>]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### LBNoProbe
```
Add-AzureEndpoint [-Name] <String> [-Protocol] <String> [-LocalPort] <Int32> [-PublicPort <Int32>]
 [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] -LBSetName <String> [-NoProbe]
 [-InternalLoadBalancerName <String>] [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>]
 [-VirtualIPName <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### LBDefaultProbe
```
Add-AzureEndpoint [-Name] <String> [-Protocol] <String> [-LocalPort] <Int32> [-PublicPort <Int32>]
 [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] -LBSetName <String> [-DefaultProbe]
 [-InternalLoadBalancerName <String>] [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>]
 [-VirtualIPName <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### LBCustomProbe
```
Add-AzureEndpoint [-Name] <String> [-Protocol] <String> [-LocalPort] <Int32> [-PublicPort <Int32>]
 [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] -LBSetName <String> -ProbePort <Int32>
 -ProbeProtocol <String> [-ProbePath <String>] [-ProbeIntervalInSeconds <Int32>]
 [-ProbeTimeoutInSeconds <Int32>] [-InternalLoadBalancerName <String>] [-IdleTimeoutInMinutes <Int32>]
 [-LoadBalancerDistribution <String>] [-VirtualIPName <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Leírás
Az **Add-AzureEndpoint** parancsmag az Azure Virtual Machine-objektum végpontját adja hozzá.

## Példák

### 1. példa: végpont hozzáadása
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirutalMachine01" | Add-AzureEndpoint -Name "HttpIn" -Protocol "tcp" -PublicPort 80 -LocalPort 8080 | Update-AzureVM
```

Ez a parancs a **Get-AzureVM** parancsmag használatával lekérdezi a VirtualMachine01 nevű virtuális gép konfigurációját.
A parancs a csővezeték-kezelő segítségével átadja az aktuális parancsmagnak.
Ez a parancsmag hozzáadja a HttpIn nevű végpontot.
A végponthoz tartozik egy 80-es nyilvános port és a 8080-es helyi port.
A parancs átadja a virtuális gép objektumát a **Update-AzureVM** parancsmagnak, amely végrehajtja a módosításokat.

### 2. példa: terheléselosztási csoportba tartozó végpont felvétele
```
PS C:\> Get-AzureVM -ServiceName "LoadBalancedService" -Name "VirtualMachine12" | Add-AzureEndpoint -Name "HttpIn" -Protocol "tcp" -PublicPort 80 -LocalPort 8080 -LBSetName "WebFarm" -ProbePort 80 -ProbeProtocol "http" -ProbePath '/' | Update-AzureVM
```

Ez a parancs beolvassa a VirtualMachine07 nevű virtuális gép konfigurációját.
Az aktuális parancsmag hozzáadja a HttpIn nevű végpontot.
A végponthoz tartozik egy 80-es nyilvános port és a 8080-es helyi port.
A végpont a webfarm nevű megosztott terheléselosztási csoportba tartozik.
Egy HTTP-szonda a 80-es porton, ahol a "/" elérési út követi a végpont elérhetőségét.
A parancs végrehajtja a módosításokat.

### 3. példa: virtuális IP hozzárendelése végponthoz
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine25" | Add-AzureEndpoint -Name "HttpIn" -Protocol "tcp" -LocalPort 8080 -PublicPort 80 -VirtualIPName "ContosoVip11" | Update-AzureVM
```

Ez a parancs beolvassa a VirtualMachine25 nevű virtuális gép konfigurációját.
Az aktuális parancsmag hozzáadja a HttpIn nevű végpontot.
A végponthoz tartozik egy 80-es nyilvános port és a 8080-es helyi port.
Ez a parancs egy virtuális IP-címet társít a végponthoz.
A parancs végrehajtja a módosításokat.

## PARAMÉTEREK

### -ACL
A végponthoz tartozó hozzáférés-vezérlési lista (ACL) beállítása.

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

### -DefaultProbe
Azt jelzi, hogy ez a parancsmag az alapértelmezett szonda beállítást használja.

```yaml
Type: SwitchParameter
Parameter Sets: LBDefaultProbe
Aliases: 

Required: True
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
A végponthoz tartozó TCP Idle időtúllépési időszakát adja meg percben.

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
A belső terheléselosztó nevét adja meg.

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
A végponthoz tartozó terheléselosztó halmaz nevét adja meg.

```yaml
Type: String
Parameter Sets: LBNoProbe, LBDefaultProbe, LBCustomProbe
Aliases: LoadBalancedEndpointSetName

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
A végpont által használt helyi, privát portot adja meg.
A virtuális gépen futó alkalmazások ebben a portban figyelik ezt a portot a végponthoz tartozó szolgáltatási kérelmekben.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (név)
A végpont nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Probléma
Azt jelzi, hogy ez a parancsmag a No Probe beállítást használja.

```yaml
Type: SwitchParameter
Parameter Sets: LBNoProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProbeIntervalInSeconds
A végponthoz tartozó valószínűségi lekérdezési intervallumot adja meg másodpercben.

```yaml
Type: Int32
Parameter Sets: LBCustomProbe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProbePath
A HTTP-szonda relatív elérési útját adja meg.

```yaml
Type: String
Parameter Sets: LBCustomProbe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProbePort
A végpont által használt portot adja meg.

```yaml
Type: Int32
Parameter Sets: LBCustomProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProbeProtocol
A port protokollt adja meg.
Az érvényes értékek a következők: 

- TCP 
- http

```yaml
Type: String
Parameter Sets: LBCustomProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProbeTimeoutInSeconds
A szondával való szavazás időpontját másodpercben kifejezve adja meg.

```yaml
Type: Int32
Parameter Sets: LBCustomProbe
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
A végpont protokollját adja meg.
Az érvényes értékek a következők: 

- TCP 
- UDP

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
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

### -VirtualIPName
Annak a virtuális IP-címnek a nevét adja meg, amely az Azure-t a végponthoz társítja.
A szolgáltatás több virtuális IP-t is tartalmazhat.
A virtuális IP-k létrehozásához használja az **Add-AzureVirtualIP** parancsmagot.

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

### -VM
Annak a virtuális gépnek a megadása, amelyhez a végpont tartozik.

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

### System. Object (rendszer. objektum)

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzureVirtualIP](./Add-AzureVirtualIP.md)

[Get-AzureEndpoint](./Get-AzureEndpoint.md)

[Get-AzureVM](./Get-AzureVM.md)

[Remove-AzureEndpoint](./Remove-AzureEndpoint.md)

[Set-AzureEndpoint](./Set-AzureEndpoint.md)

[Update-AzureVM](./Update-AzureVM.md)


