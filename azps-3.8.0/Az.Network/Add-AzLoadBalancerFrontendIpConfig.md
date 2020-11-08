---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 07FF274A-F365-44E5-A66B-6740CD165664
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 7596dff276a4913dd1c322ad023ebfb32b8e1aac
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011041"
---
# Add-AzLoadBalancerFrontendIpConfig

## Áttekintés
Az előtér IP-konfigurációját hozzáadja a terheléselosztó beállításhoz.

## SZINTAXISA

### SetByResourceSubnet (alapértelmezett)
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByResourceIdSubnet
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByResourceIdPublicIpAddress
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetByResourcePublicIpAddress
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddress <PSPublicIpAddress> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Leírás
Az **Add-AzLoadBalancerFrontendIpConfig** parancsmag egy előtér-IP-konfigurációt ad az Azure terheléselosztó szolgáltatáshoz.

## Példák

### Példa: az előtér IP-konfigurációjának hozzáadása dinamikus IP-címmel
```
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyRg" | Get-AzVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet | Set-AzLoadBalancer
```

Az első parancs beolvassa a MyVnet nevű Azure virtuális hálózatot, és az eredményt átadja a **Get-AzVirtualNetworkSubnetConfig** parancsmaggal, hogy a MySubnet nevű alhálózatot kapja.
A parancs ekkor az eredményt az $Subnet nevű változóban tárolja.
A második parancs beolvassa a MyLB nevű terheléselosztást, és az eredményt átadja az **Add-AzLoadBalancerFrontendIpConfig** parancsmagnak, amely az előtér IP-konfigurációját hozzáadja a terheléselosztáshoz egy, a $MySubnet nevű változóban tárolt dinamikus magánhálózati IP-címmel.

### Példa 2 az előtér IP-konfigurációjának hozzáadása statikus IP-címmel
```
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "RG001" | Get-AzVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet -PrivateIpAddress "10.0.1.6" | Set-AzLoadBalancer
```

Az első parancs beolvassa a MyVnet nevű Azure virtuális hálózatot, és az eredményt átadja a **Get-AzVirtualNetworkSubnetConfig** parancsmaggal, hogy a MySubnet nevű alhálózatot kapja.
A parancs ekkor az eredményt az $Subnet nevű változóban tárolja.
A második parancs beolvassa a MyLB nevű terheléselosztást, és az eredményt átadja az **Add-AzLoadBalancerFrontendIpConfig** parancsmagnak, amely az előtér IP-konfigurációját hozzáadja a terheléselosztáshoz egy, az $subnet nevű változóban tárolt statikus magánhálózati IP-címmel.

### Példa 3 előtér IP-konfigurációjának hozzáadása nyilvános IP-címmel
```
PS C:\>$PublicIp = Get-AzPublicIpAddress -ResourceGroupName "myRG" -Name "MyPub"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -PublicIpAddress $PublicIp | Set-AzLoadBalancer
```

Az első parancs a MyPub nevű Azure nyilvános IP-címet kapja, és az eredményt az $PublicIp nevű változóban tárolja.
A második parancs beolvassa a MyLB nevű terheléselosztást, és az eredményt átadja az **Add-AzLoadBalancerFrontendIpConfig** parancsmagnak, amely az előtér IP-konfigurációját hozzáadja a terheléselosztáshoz az $PublicIp nevű változóban tárolt nyilvános IP-címmel.

## PARAMÉTEREK

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

### -LoadBalancer
Egy **LoadBalancer** -objektumot ad meg.
Ez a parancsmag az előtér IP-konfigurációját hozzáadja a paraméter által megadott terheléselosztó típushoz.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Name (név)
A hozzáadni kívánt előtér IP-konfigurációjának nevét adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrivateIpAddress
Annak a magánhálózati IP-címnek a megadása, amelyet előtér-IP-konfigurációhoz szeretne társítani.

```yaml
Type: System.String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PrivateIpAddressVersion
Az IP-konfiguráció privát IP-cím verziója.

```yaml
Type: System.String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicIpAddress
Annak a nyilvános IP-címnek a megadása, amelyet előtér-IP-konfigurációhoz szeretne társítani.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResourcePublicIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicIpAddressId
Annak a nyilvános IP-címnek az AZONOSÍTÓját adja meg, amelybe be szeretné szúrni az előtér IP-konfigurációját.

```yaml
Type: System.String
Parameter Sets: SetByResourceIdPublicIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Alhálózat
Annak az alhálózati objektumnak a meghatározása, amelyben az előtér-IP-konfigurációt fel szeretné venni.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResourceSubnet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### – NetI
Annak az alhálózatnak az AZONOSÍTÓját adja meg, amelybe be szeretné szúrni az előtér IP-konfigurációját.

```yaml
Type: System.String
Parameter Sets: SetByResourceIdSubnet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Zone (zóna)
Az erőforráshoz hozzárendelt IP-címet jelölő elérhetőségi zónák listája.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
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

### Microsoft. Azure. commands. Network. models. PSLoadBalancer

### System. String

### System. string []

### Microsoft. Azure. commands. Network. models. PSSubnet

### Microsoft. Azure. commands. Network. models. PSPublicIpAddress

## KIMENETEK

### Microsoft. Azure. commands. Network. models. PSLoadBalancer

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzLoadBalancerFrontendIpConfig](./Get-AzLoadBalancerFrontendIpConfig.md)

[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)

[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)

[Új – AzLoadBalancerFrontendIpConfig](./New-AzLoadBalancerFrontendIpConfig.md)

[Remove-AzLoadBalancerFrontendIpConfig](./Remove-AzLoadBalancerFrontendIpConfig.md)

[Set-AzLoadBalancerFrontendIpConfig](./Set-AzLoadBalancerFrontendIpConfig.md)


