---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9160A21D-0F83-415B-830B-F35C8B863E90
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: a69f0d4056eb49f078c1e64342a1b4b2a8dae9ad
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339401"
---
# Add-AzNetworkSecurityRuleConfig

## SYNOPSIS
Hálózati biztonsági szabály konfigurációját ad hozzá egy hálózati biztonsági csoporthoz.

## SZINTAXIS

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

## LEÍRÁS
Az **Add-AzNetworkSecurityRuleConfig** parancsmag hálózati biztonsági szabálykonfigurációt ad egy Azure-hálózati biztonsági csoporthoz.

## PÉLDÁK

### 1: Hálózati biztonsági csoport hozzáadása
```
Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 | 
Add-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access 
    Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet 
    -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389 | 
    Set-AzNetworkSecurityGroup
```

Az első parancs lekéri az "rg1" erőforráscsoportból az "nsg1" nevű Azure-hálózat biztonsági csoportját. A második parancs hozzáad egy "rdp-rule" nevű hálózati biztonsági szabályt, amely lehetővé teszi az internetről a 3389-es porton keresztüli forgalmat a lekért hálózati biztonsági csoport objektumhoz. A módosított Azure-hálózat biztonsági csoport megőrzve.

### 2: Új biztonsági szabály hozzáadása alkalmazásbiztonsági csoportokkal
```
$srcAsg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name srcAsg -Location "West US"
$destAsg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name destAsg -Location "West US"

Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 |
Add-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access
    Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceApplicationSecurityGroup
    $srcAsg -SourcePortRange * -DestinationApplicationSecurityGroup $destAsg -DestinationPortRange 3389 |
Set-AzNetworkSecurityGroup
```

Először két új alkalmazásbiztonsági csoportot hozunk létre. Ezután lekérünk egy "nsg1" nevű Azure-hálózatbiztonsági csoportot az "rg1" erőforráscsoportból. és adjon hozzá egy "rdp-rule" nevű hálózati biztonsági szabályt. A szabály lehetővé teszi az "srcAsg" alkalmazásbiztonsági csoport összes IP-konfigurációjából a 3389-es porton található "destAsg" IP-konfigurációkba való forgalmat. A szabály hozzáadása után megmarad a módosított Azure-hálózat biztonsági csoport.

## PARAMETERS

### -Access
Azt adja meg, hogy engedélyezett vagy megtagadható-e a hálózati forgalom.
A paraméter elfogadható értékei: Allow és Deny.

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
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.

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
Megadja egy hálózati biztonsági szabály konfigurációjának leírását.

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
Megadja a célcím előtagját.
A paraméter elfogadható értékei a következőek:
- A Classless Interdomain Routing (CIDR) address
- Cél IP-címtartomány
- Helyettesítő karakter (*) bármely IP-címhez. Használhat például VirtualNetwork, AzureLoadBalancer és Internet címkéket.

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
A szabály célhelyének beállított alkalmazásbiztonsági csoport. A "DestinationAddressPrefix" paraméterrel nem használható.

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
A szabály célhelyének beállított alkalmazásbiztonsági csoport. A "DestinationAddressPrefix" paraméterrel nem használható.

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
Célportot vagy tartományt ad meg.
A paraméter elfogadható értékei a következőek:
- Egész szám
- A 0 és 65535 közötti egész számtartomány
- Egy tetszőleges portnak megfelelő helyettesítő karakter (*)

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
Meghatározza, hogy egy szabály kiértékelve legyen-e a bejövő vagy kimenő forgalom esetén.
A paraméter elfogadható értékei a következőek: Bejövő és Kimenő.

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

### -Name
Egy hálózati biztonsági szabály konfigurációjának nevét adja meg.

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
**NetworkSecurityGroup-objektumot ad** meg.
Ez a parancsmag hálózati biztonsági szabálykonfigurációt ad a paraméterként megadott objektumhoz.

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

### -Priority
Meghatározza egy szabálykonfiguráció prioritását.
A paraméter elfogadható értékei: Egy 100 és 4096 közötti egész szám.
A prioritásszámnak egyedinek kell lennie a gyűjtemény minden egyes szabályában.
Minél kisebb a prioritási szám, annál nagyobb a szabály prioritása.

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
Azt a hálózati protokollt adja meg, amelyre a szabálykonfiguráció érvényes.
A paraméter elfogadható értékei a következőek:
- Tcp
- Udp
- Helyettesítő karakter (*) mindkét karakterhez

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
Megadja a forráscím előtagját.
A paraméter elfogadható értékei a következőek:
- A CIDR
- Forrás IP-tartomány
- Egy tetszőleges IP-címnek megfelelő helyettesítő karakter (*).
Használhat olyan címkéket is, mint a VirtualNetwork, az AzureLoadBalancer és az internet.

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
A szabály forrásaként beállított alkalmazásbiztonsági csoport. A "SourceAddressPrefix" paraméterrel nem használható.

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
A szabály forrásaként beállított alkalmazásbiztonsági csoport. A "SourceAddressPrefix" paraméterrel nem használható.

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
Egy forrásportot vagy -tartományt ad meg.
Ezt az értéket egész számként, 0 és 65535 közötti tartományként, illetve helyettesítő karakterként (*) fejezi ki a forrásportok egyezéseként.

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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup

## KIMENETEK

### Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzNetworkSecurityRuleConfig](./Get-AzNetworkSecurityRuleConfig.md)

[New-AzNetworkSecurityRuleConfig](./New-AzNetworkSecurityRuleConfig.md)

[Remove-AzNetworkSecurityRuleConfig](./Remove-AzNetworkSecurityRuleConfig.md)

[Set-AzNetworkSecurityRuleConfig](./Set-AzNetworkSecurityRuleConfig.md)


