---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EFFFF43-501E-4955-A4EE-2C09B8863B30
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 42f92e7f90e5349c116f8a6ed948ed7a29a35ad2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479903"
---
# Set-AzNetworkSecurityRuleConfig

## SYNOPSIS
Egy hálózati biztonsági csoport hálózati biztonsági szabálykonfigurációját frissíti.

## SZINTAXIS

### SetByResource (alapértelmezett)
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResourceId
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroupId <String[]>] [-DestinationApplicationSecurityGroupId <String[]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## LEÍRÁS
A **Set-AzNetworkSecurityRuleConfig** parancsmag frissíti egy hálózati biztonsági szabály konfigurációját egy hálózati biztonsági csoportban.

## PÉLDÁK

### 1. példa: Hozzáférési konfiguráció módosítása hálózati biztonsági szabályban
```powershell
PS C:\>$nsg = Get-AzNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
PS C:\> $nsg | Get-AzNetworkSecurityRuleConfig -Name "rdp-rule"
PS C:\> Set-AzNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg -Access "Deny"
```

Az első parancs leküldi az NSG-FrontEnd nevű hálózati biztonsági csoportot, majd a helyi $nsg.
A második parancs a folyamatművelettel adja át a biztonsági csoportot az $nsg Get-AzNetworkSecurityRuleConfig szolgáltatásnak, amely megkapja az rdp-rule nevű biztonsági szabály-konfigurációt.
A harmadik parancs az RDP-szabály hozzáférési konfigurációját Elutasításra módosítja.

### 2. példa

Egy hálózati biztonsági csoport hálózati biztonsági szabálykonfigurációját frissíti. (automatikusan generált)

<!-- Aladdin Generated Example -->
```powershell
Set-AzNetworkSecurityRuleConfig -Access Allow -DestinationAddressPrefix * -DestinationPortRange 3389 -Direction Inbound -Name 'rdp-rule' -NetworkSecurityGroup <PSNetworkSecurityGroup> -Priority 1 -Protocol Tcp -SourceAddressPrefix 'Internet' -SourcePortRange *
```

## PARAMETERS

### -Access
Azt adja meg, hogy engedélyezett vagy megtagadható-e a hálózati forgalom. A paraméter elfogadható értékei: Allow és Deny.

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
Megadja a szabálykonfiguráció leírását.
A maximális méret 140 karakter.

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
- Helyettesítő karakter (*) egy tetszőleges porthoz

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
Meghatározza, hogy egy szabály kiértékelve legyen-e a bejövő vagy kimenő forgalomra.
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
A parancsmag által megadott hálózati biztonsági szabály-konfiguráció nevét adja meg.

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
Azt a **NetworkSecurityGroup-objektumot** adja meg, amely a beállítani kívánt hálózati biztonsági szabály-konfigurációt tartalmazza.

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
A paraméter elfogadható értékei: 100 és 4096 közötti egész szám.
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
A paraméter elfogadható értékei: --Tcp
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
- Egy tetszőleges IP-címnek megfelelő helyettesítő karakter (*). Használhat olyan címkéket is, mint a VirtualNetwork, az AzureLoadBalancer és az Internet.

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
A forrásportot vagy -tartományt adja meg.
A paraméter elfogadható értékei a következőek:
- Egész szám
- A 0 és 65535 közötti egész számtartomány
- Helyettesítő karakter (*) egy tetszőleges porthoz

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

[Add-AzNetworkSecurityRuleConfig](./Add-AzNetworkSecurityRuleConfig.md)

[Get-AzNetworkSecurityRuleConfig](./Get-AzNetworkSecurityRuleConfig.md)

[New-AzNetworkSecurityRuleConfig](./New-AzNetworkSecurityRuleConfig.md)

[Remove-AzNetworkSecurityRuleConfig](./Remove-AzNetworkSecurityRuleConfig.md)


