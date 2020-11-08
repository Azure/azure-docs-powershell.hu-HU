---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 4A0442F9-F420-4A26-9127-4C875090CC12
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0e2709ce2939cb45200e758563e917675894e443
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015724"
---
# Add-AzureInternalLoadBalancer

## Áttekintés
Belső terheléselosztást ad hozzá egy Azure-szolgáltatáshoz.

## SZINTAXISA

### ServiceAndSlot (alapértelmezett)
```
Add-AzureInternalLoadBalancer [-InternalLoadBalancerName] <String> [-ServiceName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### SubnetNameOnly
```
Add-AzureInternalLoadBalancer [-InternalLoadBalancerName] <String> [-ServiceName] <String>
 [-SubnetName] <String> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### SubnetNameAndIP
```
Add-AzureInternalLoadBalancer [-InternalLoadBalancerName] <String> [-ServiceName] <String>
 [-SubnetName] <String> [-StaticVNetIPAddress] <IPAddress> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Leírás
Az **Add-AzureInternalLoadBalancer** parancsmag belső terheléselosztási konfigurációt ad egy Azure-szolgáltatáshoz.
Virtuális hálózat esetén megadhatja a belső terheléselosztó alhálózatát vagy IP-címét.

## Példák

### Példa 1: belső terheléselosztó hozzáadása
```
PS C:\> Add-AzureInternalLoadBalancer -ServiceName "ContosoWebsite01" -InternalLoadBalancerName "ContosoILB"
```

Ez a parancs hozzáadja a ContosoILB nevű belső terheléselosztó szolgáltatást a ContosoWebsite01 nevű szolgáltatáshoz.

### 2. példa: belső terheléselosztó beállítása adott alhálózathoz
```
PS C:\> Add-AzureInternalLoadBalancer -ServiceName "ContosoWebsite01" -InternalLoadBalancerName "ContosoILB" -SubnetName "FrontEndSubnet"
```

Ez a parancs hozzáadja a ContosoILB nevű belső terheléselosztó szolgáltatást a ContosoWebsite01 nevű szolgáltatáshoz.
A parancs a FrontEndSubnet nevű alhálózatot adja meg.

### 3. példa: belső terheléselosztó beállítása meghatározott alhálózathoz és címhez
```
PS C:\> Add-AzureInternalLoadBalancer -ServiceName "ContosoWebsite01" -InternalLoadBalancerName "ContosoILB" -SubnetName "FrontEndSubnet" -StaticVNetIPAddress 192.168.4.7
```

Ez a parancs hozzáadja a ContosoILB nevű belső terheléselosztó szolgáltatást a ContosoWebsite01 nevű szolgáltatáshoz.
A parancs a FrontEndSubnet nevű alhálózatot és a virtuális hálózat statikus címét adja meg.

## PARAMÉTEREK

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
Annak a belső terheléselosztásnak a neve, amelyet a parancsmag ad.

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

### -Szolgáltatásnév
Annak a szolgáltatásnak a nevét adja meg, amelyre a parancsmag egy belső terheléselosztó bővítményt ad.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StaticVNetIPAddress
Megadja a parancsmag által hozzáadott belső terheléselosztó virtuális hálózati IP-címét.

```yaml
Type: IPAddress
Parameter Sets: SubnetNameAndIP
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubnetName
Annak az alhálózatnak a nevét adja meg, amely a parancsmag által hozzáadott belső terheléselosztást tartalmazza.

```yaml
Type: String
Parameter Sets: SubnetNameOnly, SubnetNameAndIP
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

### Microsoft. WindowsAzure. commands. Utilities. Common. ManagementOperationContext

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureInternalLoadBalancer](./Get-AzureInternalLoadBalancer.md)

[Új – AzureInternalLoadBalancerConfig](./New-AzureInternalLoadBalancerConfig.md)

[Remove-AzureInternalLoadBalancer](./Remove-AzureInternalLoadBalancer.md)

[Set-AzureInternalLoadBalancer](./Set-AzureInternalLoadBalancer.md)


