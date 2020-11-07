---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallnetworkrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRuleCollection.md
ms.openlocfilehash: af0a81cf915cd853bfc8ca957d706cdb45d96180
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670334"
---
# New-AzFirewallNetworkRuleCollection

## Áttekintés
Azure-tűzfal hálózati gyűjteményét hozza létre hálózati szabályokhoz.

## SZINTAXISA

```
New-AzFirewallNetworkRuleCollection -Name <String> -Priority <UInt32> -Rule <PSAzureFirewallNetworkRule[]>
 -ActionType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
A **New-AzFirewallNetworkRuleCollection** parancsmag tűzfal-hálózati szabályok gyűjteményét hozza létre.

## Példák

### 1: egy hálózati gyűjtemény létrehozása két szabállyal
```
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$rule2 = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
New-AzFirewallNetworkRuleCollection -Name RC1 -Priority 100 -Rule $rule1, $rule2 -ActionType "Allow"
```

Ez a példa olyan gyűjteményt hoz létre, amely lehetővé teszi az összes olyan adatforgalom beállítását, amely megfelel a két szabály egyikének.
Az első szabály az összes UDP-forgalom esetén használható.
A második szabály a 10.0.0.0-től a 60.1.5.0-ig való TCP-forgalom: 4040.
Ha létezik olyan hálózati szabály gyűjteménye, amely magasabb prioritással (kisebb számmal) rendelkezik, és a $rule 1 vagy $rule 2 értékben megjelölt forgalmat is megegyeznek, a magasabb prioritású szabály-gyűjteményben szereplő műveletek inkább az eredményben lépnek. 

### 2: szabály hozzáadása egy szabály-gyűjteményhez
```
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$ruleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"

$rule2 = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
$ruleCollection.AddRule($rule2)
```

Ebben a példában egy új hálózati szabály-gyűjtemény jön létre egy szabállyal, majd egy második szabályt ad hozzá a szabályok gyűjteményéhez a szabály-gyűjtemény AddRule. A megadott szabálygyűjtemény minden szabályának egyedi névvel kell rendelkeznie, és a kis-és nagybetűk megkülönböztetését is megadhatja.

### 3: szabály kérése egy szabály-gyűjteményből
```
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$ruleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"
$getRule=$ruleCollection.GetRuleByName("ALL-UDP-traffic")
```

Ebben a példában egy új hálózati szabály-gyűjtemény jön létre egy szabállyal, majd a szabályt név szerint, a hívási módszer GetRuleByName a szabály-gyűjtemény objektumon kapja. A GetRuleByName metódus szabályának neve megkülönbözteti a kis-és nagybetűket.

### 4: szabály eltávolítása a szabályok gyűjteményéből
```
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$rule2 = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
$ruleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1, $rule2 -ActionType "Allow"
$ruleCollection.RemoveRuleByName("ALL-udp-traffic")
```

Ebben a példában egy új hálózati szabály-gyűjtemény jön létre két szabállyal, majd eltávolítja az első szabályt a szabály gyűjteményből a RemoveRuleByName metódust. A RemoveRuleByName metódus szabályának neve megkülönbözteti a kis-és nagybetűket.

## PARAMÉTEREK

### -ActionType
Megadja, hogy milyen műveletek szükségesek a szabály forgalmi feltételeihez. Az elfogadott műveletek "Allow" vagy "deny".

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

### -Name (név)
A hálózati szabály-gyűjtemény nevét adja meg. A névnek minden hálózati szabály-gyűjteményben egyedinek kell lennie.

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

### – Prioritás
A szabály-gyűjtemény prioritását adja meg. A prioritás az 100 és az 65000 közötti szám. Minél kisebb a szám, annál nagyobb a prioritás.

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

### -Szabály
Az ebben a gyűjteményben csoportosítani kívánt szabályok listáját adja meg.

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

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

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
Annak megjelenítése, hogy mi történik, ha a parancsmag fut.
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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs

## KIMENETEK

### Microsoft. Azure. commands. Network. models. PSAzureFirewallNetworkRuleCollection

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzFirewallNetworkRule](./New-AzFirewallNetworkRule.md)

[Új – AzFirewall](./New-AzFirewall.md)

[Get-AzFirewall](./Get-AzFirewall.md)
