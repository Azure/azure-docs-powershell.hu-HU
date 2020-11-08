---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1BA472FB-E684-486C-8066-42C9215DBDEF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 83d1afcae66af7e4548b1dbd4031392969f4d267
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016057"
---
# Set-AzureEndpoint

## Áttekintés
Módosítja egy virtuális géphez rendelt végpontot.

## SZINTAXISA

```
Set-AzureEndpoint [-Name] <String> [[-Protocol] <String>] [[-LocalPort] <Int32>] [-PublicPort <Int32>]
 [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] [-InternalLoadBalancerName <String>]
 [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>] [-VirtualIPName <String>]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Leírás
A **set-AzureEndpoint** parancsmag módosította az Azure Virtual Machine rendszerhez rendelt végpontot.
Megadhatja az olyan végpontok módosításait is, amelyek nem töltődnek be a terheléselosztásban.

## Példák

### 1. példa: a végpontok módosítása a port figyeléséhez
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirutalMachine01" | Set-AzureEndpoint -Name "Web" -PublicPort 443 -LocalPort 443 -Protocol tcp | Update-AzureVM
```

Ez a parancs a **Get-AzureVM** parancsmag használatával lekérdezi a VirtualMachine01 nevű virtuális gép konfigurációját.
A parancs a csővezeték-kezelő segítségével átadja az aktuális parancsmagnak.
Ez a parancsmag módosítja a Web nevű végpontot a 443-es port figyeléséhez.
A parancs átadja a virtuális gép objektumát a **Update-AzureVM** parancsmagnak, amely végrehajtja a módosításokat.

## PARAMÉTEREK

### -ACL
Olyan hozzáférés-vezérlési lista (ACL) konfigurációs objektumát adja meg, amelyre a parancsmag érvényes a végpontra.

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

Required: False
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

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicPort
A végpont által használt nyilvános portot adja meg.

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

[Add-AzureEndpoint](./Add-AzureEndpoint.md)

[Add-AzureVirtualIP](./Add-AzureVirtualIP.md)

[Get-AzureEndpoint](./Get-AzureEndpoint.md)

[Get-AzureVM](./Get-AzureVM.md)

[Remove-AzureEndpoint](./Remove-AzureEndpoint.md)

[Update-AzureVM](./Update-AzureVM.md)


