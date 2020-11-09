---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 92F192A5-F75E-4EFE-B2D2-B0DF0B78D3B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpConfig.md
ms.openlocfilehash: e2ca08746ab9b4dc2ef2265a59cdab00ac42cf33
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300767"
---
# New-AzVmssIpConfig

## Áttekintés
IP-konfigurációt hoz létre egy VMSS hálózati felületéhez.

## SZINTAXISA

```
New-AzVmssIpConfig [[-Name] <String>] [[-Id] <String>] [[-SubnetId] <String>]
 [[-ApplicationGatewayBackendAddressPoolsId] <String[]>] [[-LoadBalancerBackendAddressPoolsId] <String[]>]
 [[-LoadBalancerInboundNatPoolsId] <String[]>] [-Primary] [-PrivateIPAddressVersion <String>]
 [-PublicIPAddressConfigurationName <String>] [-PublicIPAddressConfigurationIdleTimeoutInMinutes <Int32>]
 [-DnsSetting <String>] [-IpTag <VirtualMachineScaleSetIpTag[]>] [-PublicIPPrefix <String>]
 [-PublicIPAddressVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Leírás
A **New-AzVmssIpConfig** parancsmag létrehoz egy IP-konfigurációs objektumot a virtuálisgép-készlet (VMSS) hálózati felületéhez.
Adja meg a parancsmag konfigurációját az Add-AzVmssNetworkInterfaceConfiguration parancsmag *IPConfiguration* paramétereként.

## Példák

### Példa 1: IP-konfigurációs objektum létrehozása VMSS-felülethez
```
PS C:\> $IPConfiguration = New-AzVmssIPConfig -Name "ContosoVmssInterface02" -SubnetId $SubnetId
```

Ez a parancs létrehoz egy ContosoVmssInterface02 nevű IP-konfigurációs objektumot.
A parancs a $SubnetIdban tárolt korábban definiált alhálózati azonosítót használja.
A parancs a $IPConfiguration változóban lévő konfigurációs beállításokat az **Add-AzVmssNetworkInterfaceConfiguration** későbbi használat céljából menti.

### 2. példa: IP-konfigurációs objektum létrehozása a NAT-készlet beállításai között
```
PS C:\> $IPConfiguration = New-AzVmssIPConfig -Name "ContosoVmssInterface03" -LoadBalancerInboundNatPoolsId $expectedLb.InboundNatPools[0].Id -LoadBalancerBackendAddressPoolsId $expectedLb.BackendAddressPools[0].Id -SubnetId $SubnetId
```

Ez a parancs létrehoz egy ContosoVmssInterface03 nevű IP-konfigurációs objektumot, majd a $IPConfiguration változóban tárolja későbbi használatra.
A parancs a $SubnetIdban tárolt korábban definiált alhálózati azonosítót használja.
A parancs a $IPConfiguration változóban lévő konfigurációs beállításokat későbbi használat céljából menti.
A parancs a *LoadBalancerInboundNatPoolsId* és a *LoadBalancerBackendAddressPoolsId* paraméter értékét adja meg.

## PARAMÉTEREK

### -ApplicationGatewayBackendAddressPoolsId
A backend-címekre mutató hivatkozásokat tartalmazó tömböt ad meg.
A méretarány a backend-címkészletet egy nyilvános és egy belső terheléselosztó segítségével is hivatkozhat.
Több méretarányos készlet nem használhatja ugyanazt a terheléselosztó típust.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DnsSetting
A publicIP-címeken alkalmazandó DNS-beállítások.
A publicIP-címeken alkalmazandó DNS-beállítások tartománynév-címkéje.
A tartománynév-címke és a VM-index összefűzése a létrehozandó nyilvános IP-cím erőforrásainak tartománynév-címkéjén lesz.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PublicIPAddressDomainNameLabel

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Azonosító
AZONOSÍTÓT ad meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IpTag
Az IP-címkézett objektumok tömbjét adja meg.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LoadBalancerBackendAddressPoolsId
A betöltők beérkező hálózati címfordítási (NAT) medencéjére mutató hivatkozások tömbjét adja meg.
A méretarányos beállítással hivatkozhat a beérkező NAT-készletekre egy nyilvános és egy belső terheléselosztó segítségével.
Több méretarányos készlet nem használhatja ugyanazt a terheléselosztó típust.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LoadBalancerInboundNatPoolsId
A terheléselosztásban beérkező NAT-készletekre mutató hivatkozások tömbjét adja meg.
A méretarányos beállítással hivatkozhat a beérkező NAT-készletekre egy nyilvános és egy belső terheléselosztó segítségével.
Több méretarányos készlet nem használhatja ugyanazt a terheléselosztó típust.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (név)
Az IP-konfiguráció nevét adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Elsődleges
Az elsődleges IP-konfigurációt adja meg abban az esetben, ha a hálózati felület több IP-konfigurációval rendelkezik.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrivateIPAddressVersion
Adja meg a magánjellegű IP-cím IP-konfigurációját.  Az alapértelmezett érték az IPv4.  A lehetséges értékek a következők: "IPv4" és "IPv6".

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicIPAddressConfigurationIdleTimeoutInMinutes
A nyilvános IP-cím üresjárati időkorlátja.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: PublicIPAddressIdleTimeoutInMinutes

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicIPAddressConfigurationName
Az publicIP név.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PublicIPAddressName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicIPAddressVersion
Adja meg a nyilvános IP-cím IP-konfigurációját.  Az alapértelmezett érték az IPv4.  A lehetséges értékek a következők: "IPv4" és "IPv6".

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicIPPrefix
A nyilvános IP-előtag azonosítója

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### – NetI
Annak az alhálózatnak az AZONOSÍTÓját adja meg, amelyben a konfiguráció létrehozta a VMSS-hálózati felületet.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Annak megjelenítése, hogy mi történik, ha a parancsmag fut. A parancsmag nem fut.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.

## BEMENETEK

### System. String

### System. string []

### System. Int32

### Microsoft. Azure. Management. számítás. models. VirtualMachineScaleSetIpTag []

## KIMENETEK

### Microsoft. Azure. Management. kiszámítás. models. VirtualMachineScaleSetIPConfiguration

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzVmssNetworkInterfaceConfiguration](./Add-AzVmssNetworkInterfaceConfiguration.md)


