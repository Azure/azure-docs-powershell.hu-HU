---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallnetworkrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRuleCollection.md
ms.openlocfilehash: 49a7484c0ca0b1a3dfa0feb82e09632d631333ed
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469017"
---
# New-AzFirewallNetworkRuleCollection

## SYNOPSIS
Létrehozza az Azure Firewall Network Network Collection of Network rules (Hálózati szabályok) gyűjteményt.

## SZINTAXIS

```
New-AzFirewallNetworkRuleCollection -Name <String> -Priority <UInt32> -Rule <PSAzureFirewallNetworkRule[]>
 -ActionType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## LEÍRÁS
A **New-AzFirewallNetworkRuleCollection** parancsmag tűzfalhálózati szabályok gyűjteményét hozza létre.

## PÉLDÁK

### 1. példa: Két szabályokkal létrehozott hálózati gyűjtemény
```powershell
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$rule2 = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
New-AzFirewallNetworkRuleCollection -Name RC1 -Priority 100 -Rule $rule1, $rule2 -ActionType "Allow"
```

Ez a példa létrehoz egy gyűjteményt, amely engedélyezi a két szabály bármelyikének megfelelő forgalmat.
Az első szabály az összes UDP-forgalomra vonatkozik.
A második szabály a 10.0.0.0 és 60.1.5.0:4040-es TCP-forgalomra vonatkozik.
Ha egy másik, magasabb prioritású (kisebb számú) szabálygyűjtemény is van, amely az $rule 1-ben vagy a $rule 2-ben azonosított forgalommal is megegyezik, akkor a magasabb prioritású szabálygyűjteményre vonatkozó művelet lép életbe. 

### 2. példa: Szabály hozzáadása szabálygyűjteményhez
```powershell
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$ruleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"

$rule2 = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
$ruleCollection.AddRule($rule2)
```

Ebben a példában létrehoz egy új hálózatszabály-gyűjteményt egy s szabály alapján, majd hozzáad egy második szabályt a szabálygyűjteményhez az AddRule metódussal a szabálygyűjtemény-objektumon. Az adott szabálygyűjteményben minden szabálynévnek egyedi névvel kell lennie, és a kis- és a nagy- és a kis

### 3. példa: Szabály begyűjtése szabálygyűjteményből
```powershell
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$ruleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"
$getRule=$ruleCollection.GetRuleByName("ALL-UDP-traffic")
```

Ebben a példában egy új hálózatszabály-gyűjteményt hoz létre egy s szabály alapján, majd név szerint getruleByName hívási metódust kap a szabálygyűjtemény-objektumon. A GetRuleByName metódus szabályneve a kis- és

### 4. példa: Szabály eltávolítása szabálygyűjteményből
```powershell
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$rule2 = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
$ruleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1, $rule2 -ActionType "Allow"
$ruleCollection.RemoveRuleByName("ALL-udp-traffic")
```

Ebben a példában egy új hálózatszabály-gyűjteményt hoz létre két sszabályokkal, majd eltávolítja az első szabályt a szabálygyűjteményből a RemoveRuleByName hívási módszerrel a szabálygyűjtemény-objektumon. A RemoveRuleByName metódus szabályneve a kis- és

## PARAMETERS

### -ActionType
Meghatározza, hogy mit kell tenni a szabályban a forgalomnak megfelelő feltételek esetén. Az elfogadott műveletek "Megengedve" vagy "Elutasítás".

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: True
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

### -Name
A hálózati szabálycsoport nevét adja meg. A névnek minden hálózati szabálycsoportban egyedinek kell lennie.

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
A szabálygyűjtemény prioritását határozza meg. A prioritás 100 és 65000 közötti szám. Minél kisebb a szám, annál nagyobb a prioritás.

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Rule
Az ebben a gyűjteményben csoportosított szabályok listáját határozza meg.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
A parancsmag futtatása előtt a rendszer megerősítést kér.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
A parancsmag futtatásakor a program megjeleníti, hogy mi történik.
A parancsmag nem fut.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Nincs

## KIMENETEK

### Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[New-AzFirewallNetworkRule](./New-AzFirewallNetworkRule.md)

[New-AzFirewall](./New-AzFirewall.md)

[Get-AzFirewall](./Get-AzFirewall.md)
