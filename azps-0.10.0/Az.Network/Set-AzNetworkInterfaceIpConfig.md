---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 13EF1028-43DE-424D-8185-EC45B5CEF2C1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 0e74aa06d2966ed4e907de7428ddc1f4d3a6f2cb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843609"
---
# Set-AzNetworkInterfaceIpConfig

## Áttekintés
Az Azure-alapú hálózati kapcsolat IP-konfigurációjának cél állapotának beállítása.

## SZINTAXISA

### SetByResource (alapértelmezett)
```
Set-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>]
 [-LoadBalancerBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]>]
 [-LoadBalancerInboundNatRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]>]
 [-ApplicationGatewayBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]>]
 [-ApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResourceId
```
Set-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-SubnetId <String>]
 [-PublicIpAddressId <String>]
 [-LoadBalancerBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-LoadBalancerInboundNatRuleId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationGatewayBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **set-AzNetworkInterfaceIpConfig** parancsmag az Azure-alapú hálózati kapcsolat IP-konfigurációjának cél állapotát állítja be.

## Példák

### 1: IP-konfiguráció IP-címének módosítása
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet

$nic = Get-AzNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet
    -Primary

$nic | Set-AzNetworkInterface
```

Az első két parancs a myvnet nevű virtuális hálózatot és egy mysubnet nevű alhálózatot hoz létre, és tárolja a változók $vnet és $subnet. A harmadik parancs a frissíteni kívánt IP-konfigurációhoz társított hálózati felület nic1 kapja. A harmadik parancs a 10.0.0.11 elsődleges IP-konfigurációs ipconfig1 privát IP-címét állítja be. Végül az utolsó parancs frissíti azt a hálózati felületet, amely biztosítja a módosítások sikeres létrejöttét.
    

### 2: IP-konfiguráció társítása alkalmazások biztonsági groupp
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet
$asg = Get-ApplicationSecurityGroup -Name myasg -ResourceGroupName myrg

$nic = Get-AzNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet -ApplicationSecurityGroup $asg
    -Primary

$nic | Set-AzNetworkInterface
```

Ebben a példában az $asg változó egy alkalmazás biztonsági csoportjának hivatkozását tartalmazza.
A negyedik parancs a frissíteni kívánt IP-konfigurációhoz társított hálózati felület nic1 kapja. A Set-AzNetworkInterfaceIpConfig az elsődleges IP-konfigurációs ipconfig1 privát IP-címét állítja be a 10.0.0.11, és létrehoz egy társítást a lekérdezett alkalmazás biztonsági csoportjához.
Végül az utolsó parancs frissíti azt a hálózati felületet, amely biztosítja a módosítások sikeres létrejöttét.

## PARAMÉTEREK

### -ApplicationGatewayBackendAddressPool
Itt adhatja meg az alkalmazás-átjáró backend-hivatkozásait, amelyekre a hálózati kapcsolat IP-konfigurációja tartozik.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ApplicationGatewayBackendAddressPoolId
Itt adhatja meg az alkalmazás-átjáró backend-hivatkozásait, amelyekre a hálózati kapcsolat IP-konfigurációja tartozik.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ApplicationSecurityGroup
Az alkalmazás biztonsági csoportjának hivatkozásait adja meg, amelyekre a hálózati kapcsolat IP-konfigurációja tartozik.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ApplicationSecurityGroupId
Az alkalmazás biztonsági csoportjának hivatkozásait adja meg, amelyekre a hálózati kapcsolat IP-konfigurációja tartozik.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LoadBalancerBackendAddressPool
A terheléselosztó backend-címeinek gyűjteményét adja meg, amelyre ez a hálózati kapcsolat IP-konfigurációja tartozik.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LoadBalancerBackendAddressPoolId
A terheléselosztó backend-címeinek gyűjteményét adja meg, amelyre ez a hálózati kapcsolat IP-konfigurációja tartozik.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LoadBalancerInboundNatRule
A terheléselosztásos bejövő hálózati címfordítási (NAT) szabályok azon hivatkozásait adja meg, amelyekre a hálózati kapcsolat IP-konfigurációja tartozik.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LoadBalancerInboundNatRuleId
A terheléselosztó bejövő NAT-szabályok hivatkozásait adja meg, amelyekre a hálózati kapcsolat IP-konfigurációja tartozik.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (név)
Annak a hálózatnak az IP-konfigurációjának a neve, amelyhez a parancsmag be van jelölve.

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

### -NetworkInterface
Egy **NetworkInterface** -objektumot ad meg.
Ez a parancsmag a hálózati kapcsolat IP-konfigurációját hozzáadja az objektumhoz, amelyhez a paraméter van meghatározva.

```yaml
Type: PSNetworkInterface
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Elsődleges
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrivateIpAddress
A hálózati kapcsolat IP-konfigurációjának statikus IP-címét adja meg.

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

### -PrivateIpAddressVersion
A hálózati kapcsolat IP-konfigurációjának IP-cím verzióját adja meg.
A paraméter elfogadható értékei a következők:

- IPv4
- IPv6

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicIpAddress
Egy **PublicIPAddress** -objektumot ad meg.
Ez a parancsmag egy olyan nyilvános IP-címre mutató hivatkozást hoz létre, amellyel társítva van ezzel a hálózati kapcsolat IP-konfigurációjával.

```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicIpAddressId
Ez a parancsmag egy olyan nyilvános IP-címre mutató hivatkozást hoz létre, amellyel társítva van ezzel a hálózati kapcsolat IP-konfigurációjával.

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Alhálózat
**Alhálózat** -objektumot ad meg.
Ez a parancsmag egy olyan alhálózatra mutató hivatkozást hoz létre, amelyben a hálózati kapcsolat IP-konfigurációja van létrehozva.

```yaml
Type: PSSubnet
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### – NetI
Ez a parancsmag egy olyan alhálózatra mutató hivatkozást hoz létre, amelyben a hálózati kapcsolat IP-konfigurációja van létrehozva.

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### PSNetworkInterface
A ' NetworkInterface ' paraméter az "PSNetworkInterface" típusú értéket fogadja el a csővezetékről

## KIMENETEK

### Microsoft. Azure. commands. Network. models. PSNetworkInterface

## MEGJEGYZI
* Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzNetworkInterfaceIpConfig](./Add-AzNetworkInterfaceIpConfig.md)

[Get-AzNetworkInterfaceIpConfig](./Get-AzNetworkInterfaceIpConfig.md)

[Új – AzNetworkInterfaceIpConfig](./New-AzNetworkInterfaceIpConfig.md)

[Remove-AzNetworkInterfaceIpConfig](./Remove-AzNetworkInterfaceIpConfig.md)


