---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 633FB5C9-BEB3-42A3-AF4F-A54CC3F9E0F7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: adef9e3a2ba0d1e67ee8cb2ec9bdd14d9833f5d7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379075"
---
# New-AzNetworkSecurityRuleConfig

## SYNOPSIS
Hálózati biztonsági szabály konfigurációját hozza létre.

## SZINTAXIS

### SetByResource (alapértelmezett)
```
New-AzNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>] [-SourceAddressPrefix <String[]>]
 [-DestinationAddressPrefix <String[]>] [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResourceId
```
New-AzNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>] [-SourceAddressPrefix <String[]>]
 [-DestinationAddressPrefix <String[]>] [-SourceApplicationSecurityGroupId <String[]>]
 [-DestinationApplicationSecurityGroupId <String[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A **New-AzNetworkSecurityRuleConfig** parancsmag létrehoz egy Azure-hálózatbiztonsági szabálykonfigurációt egy hálózati biztonsági csoporthoz.

## PÉLDÁK

### 1. példa: Az RDP-t engedélyező hálózati biztonsági szabály létrehozása
```powershell
$rule1 = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" `
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix `
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
```

Ez a parancs egy olyan biztonsági szabályt hoz létre, amely engedélyezi az internetről a 3389-es port elérését

### 2. példa: HTTP-t lehetővé tő hálózati biztonsági szabály létrehozása
```powershell
$rule2 = New-AzNetworkSecurityRuleConfig -Name web-rule -Description "Allow HTTP" `
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 101 -SourceAddressPrefix `
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 80
```

Ez a parancs egy olyan biztonsági szabályt hoz létre, amely engedélyezi az internetről a 80-as portot

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
Megadja a létrehozni szükséges hálózati biztonsági szabály konfigurációjának leírását.

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
A parancsmag által létrehozott hálózati biztonsági szabály-konfiguráció nevét adja meg.

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

### -Priority
Meghatározza a szabálykonfiguráció prioritását.
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
Azt a hálózati protokollt adja meg, amelyre az új szabálykonfiguráció érvényes.
A paraméter elfogadható értékei a következőek:
- Tcp
- Udp
- helyettesítő karakter (*) mindkét karakterhez.

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

### Nincs

## KIMENETEK

### Microsoft.Azure.Commands.Network.Models.PSSecurityRule

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzNetworkSecurityRuleConfig](./Add-AzNetworkSecurityRuleConfig.md)

[Get-AzNetworkSecurityRuleConfig](./Get-AzNetworkSecurityRuleConfig.md)

[Remove-AzNetworkSecurityRuleConfig](./Remove-AzNetworkSecurityRuleConfig.md)

[Set-AzNetworkSecurityRuleConfig](./Set-AzNetworkSecurityRuleConfig.md)


