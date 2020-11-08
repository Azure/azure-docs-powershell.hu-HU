---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9160A21D-0F83-415B-830B-F35C8B863E90
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: a69f0d4056eb49f078c1e64342a1b4b2a8dae9ad
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187054"
---
# Add-AzNetworkSecurityRuleConfig

## Áttekintés
Hálózati biztonsági szabály konfigurációjának felvétele hálózati biztonsági csoportba.

## SZINTAXISA

### SetByResource (alapértelmezett)
```
Add-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResourceId
```
Add-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroupId <String[]>] [-DestinationApplicationSecurityGroupId <String[]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
Az **Add-AzNetworkSecurityRuleConfig** parancsmag hálózati biztonsági szabály-konfigurációt ad hozzá az Azure hálózat biztonsági csoportjához.

## Példák

### 1: hálózati biztonsági csoport hozzáadása
```
Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 | 
Add-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access 
    Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet 
    -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389 | 
    Set-AzNetworkSecurityGroup
```

Az első parancs a "rg1" erőforráscsoport "nsg1" nevű Azure hálózati biztonsági csoportjának beolvasása. A második parancs hozzáadja az "RDP-szabály" nevű hálózati biztonsági szabályt, amely lehetővé teszi, hogy a 3389-on lévő internetről érkező forgalom a lekérdezett hálózati biztonsági csoport objektumba kerüljön. Megmarad a módosított Azure hálózat biztonsági csoportja.

### 2: új biztonsági szabály felvétele az alkalmazás biztonsági csoportjaival
```
$srcAsg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name srcAsg -Location "West US"
$destAsg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name destAsg -Location "West US"

Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 |
Add-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access
    Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceApplicationSecurityGroup
    $srcAsg -SourcePortRange * -DestinationApplicationSecurityGroup $destAsg -DestinationPortRange 3389 |
Set-AzNetworkSecurityGroup
```

Elsőként hozzunk létre két új alkalmazás biztonsági csoportját. Ezután egy "nsg1" nevű Azure Network biztonsági csoportot keresünk a "rg1" erőforráscsoporthoz. lehetőséget, és adjon hozzá egy "RDP-Rule" nevű hálózati biztonsági szabályt. A szabály megengedi az összes IP-beállítás forgalmát a "srcAsg" az összes IP-konfigurációból az 3389-es port "destAsg" csoportjában. Miután hozzáadta a szabályt, továbbra is fennáll a módosított Azure-hálózat biztonsági csoportja.

## PARAMÉTEREK

### -Access
Megadja, hogy engedélyezve van-e a hálózati forgalom vagy a hozzáférés visszautasítása.
A paraméter elfogadható értékei a következők: Allow és deny.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### -Leírás
A hálózati biztonsági szabályok konfigurációjának leírását adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationAddressPrefix
A célcím előtagját adja meg.
A paraméter elfogadható értékei a következők:
- Osztály nélküli tartományok közötti útválasztási (CIDR) cím
- Cél IP-címtartomány
- A helyettesítő karakter (*) tetszőleges IP-címnek megfelelő (például VirtualNetwork, AzureLoadBalancer és Internet) használható.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationApplicationSecurityGroup
Az alkalmazás biztonsági csoportja a szabály rendeltetési helyére. Az "DestinationAddressPrefix" paraméterrel nem használható.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationApplicationSecurityGroupId
Az alkalmazás biztonsági csoportja a szabály rendeltetési helyére. Az "DestinationAddressPrefix" paraméterrel nem használható.

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationPortRange
A cél portját vagy a kívánt cellatartományt adja meg.
A paraméter elfogadható értékei a következők:
- Egész szám
- 0 és 65535 közötti egész számok
- Bármely portnak megfelelő helyettesítő karakter (*)

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Irány
Azt adja meg, hogy a rendszer kiértékeli-e a szabályt a bejövő vagy kimenő forgalomban.
A paraméter elfogadható értékei a következők: bejövő és kimenő.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Inbound, Outbound

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (név)
A hálózati biztonsági szabályok konfigurációjának nevét adja meg.

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

### -NetworkSecurityGroup
Egy **NetworkSecurityGroup** -objektumot ad meg.
Ez a parancsmag hálózati biztonsági szabály konfigurációját adja hozzá az objektumhoz, amelyhez a paraméter van meghatározva.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### – Prioritás
A szabály konfigurációjának prioritását adja meg.
A paraméter elfogadható értékei a következők: az 100 és az 4096 közötti egész szám.
A prioritási számnak egyedinek kell lennie a gyűjtemény mindegyik szabályához.
Minél alacsonyabb a prioritási szám, annál nagyobb a szabály prioritása.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Protocol
Azt a hálózati protokollt adja meg, amelyre a szabály konfigurációja vonatkozik.
A paraméter elfogadható értékei a következők:
- TCP
- UDP
- Helyettesítő karakter (*) a két érték egyeztetéséhez

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Tcp, Udp, *

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceAddressPrefix
A forráscím előtagját adja meg.
A paraméter elfogadható értékei a következők:
- CIDR
- A forrás IP-köre
- Egy helyettesítő karakter (*) az IP-cím megegyezéséhez.
A címkéket (például VirtualNetwork, AzureLoadBalancer és Internet) is használhatja.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceApplicationSecurityGroup
Az alkalmazás biztonsági csoportja a szabály forrásaként van beállítva. Az "SourceAddressPrefix" paraméterrel nem használható.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceApplicationSecurityGroupId
Az alkalmazás biztonsági csoportja a szabály forrásaként van beállítva. Az "SourceAddressPrefix" paraméterrel nem használható.

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourcePortRange
A forrás-portot vagy-cellatartományt adja meg.
Ezt az értéket egész számként fejezi ki, 0 és 65535 közötti tartománnyal, vagy helyettesítő karakterként (*), amely a forrás-porthoz igazodik.

```yaml
Type: System.String[]
Parameter Sets: (All)
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

### Microsoft. Azure. commands. Network. models. PSNetworkSecurityGroup

## KIMENETEK

### Microsoft. Azure. commands. Network. models. PSNetworkSecurityGroup

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzNetworkSecurityRuleConfig](./Get-AzNetworkSecurityRuleConfig.md)

[Új – AzNetworkSecurityRuleConfig](./New-AzNetworkSecurityRuleConfig.md)

[Remove-AzNetworkSecurityRuleConfig](./Remove-AzNetworkSecurityRuleConfig.md)

[Set-AzNetworkSecurityRuleConfig](./Set-AzNetworkSecurityRuleConfig.md)


