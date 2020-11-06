---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A3D60CF1-2E66-4EE5-9C68-932DD8DF80BD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewall.md
ms.openlocfilehash: 6486c7db87e8c71b0703b90a765fa30287b82769
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504356"
---
# New-AzureRmFirewall

## Áttekintés
Új tűzfal létrehozása egy erőforrás-csoportban

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
New-AzureRmFirewall -Name <String> -ResourceGroupName <String> -Location <String>
 [-VirtualNetworkName <String>] [-PublicIpName <String>]
 [-ApplicationRuleCollection <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection]>]
 [-NatRuleCollection <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection]>]
 [-NetworkRuleCollection <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Leírás
A **New-AzureRmFirewall** parancsmag Azure-tűzfalat hoz létre.

## Példák

### 1: virtuális hálózathoz kapcsolt tűzfal létrehozása
```
New-AzureRmFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -VirtualNetworkName "vnet" -PublicIpName "pip-name"
```

Ez a példa létrehoz egy olyan tűzfalat, amely a "vnet" virtuális hálózathoz van csatolva a tűzfalban lévő erőforrás-csoportban.
Mivel nincs megadva szabály, a tűzfal letiltja az összes forgalmat (alapértelmezett viselkedés).

### 2: tűzfal létrehozása, amely lehetővé teszi az összes HTTPS-forgalmat
```
$rule = New-AzureRmFirewallApplicationRule -Name R1 -Protocol "https:443" -TargetFqdn "*" 
$ruleCollection = New-AzureRmFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzureRmFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -VirtualNetworkName "vnet" -PublicIpName "pip-name" -ApplicationRuleCollection $ruleCollection
```

Ez a példa létrehoz egy tűzfalat, amely lehetővé teszi az összes HTTPS-forgalmat a 443-es porton keresztül.

### 3: DNAT-átirányítja a forgalmat a 10.1.2.3:80 – 10.2.3.4:8080
```
$rule = New-AzureRmFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.2.3.4" -TranslatedPort "8080"
$ruleCollection = New-AzureRmFirewallNatRuleCollection -Name "NatRuleCollection" -Priority 1000 -Rule $rule
New-AzureRmFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -NatRuleCollection $ruleCollection
```

Ez a példa létrehozta azt a tűzfalat, amely lefordította az 10.1.2.3-ra szánt összes csomag cél IP-címe és portja: 10.2.3.4:8080

## PARAMÉTEREK

### -ApplicationRuleCollection
Az új tűzfalhoz tartozó alkalmazási szabályok gyűjteményét adja meg.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AsJob
A parancsmag futtatása a háttérben

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

### -Force
Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.

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

### -Hely
A tűzfal régióját adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (név)
Annak az Azure-tűzfalnak a neve, amelyet a parancsmag hoz létre.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NatRuleCollection
A AzureFirewallNatRuleCollections listája

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NetworkRuleCollection
A AzureFirewallNetworkRuleCollections listája

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicIpName
Nyilvános IP-név. A nyilvános IP-nek a standard SKU-nak kell lennie, és ugyanahhoz az erőforrás csoporthoz kell tartoznia, mint a tűzfalnak.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Annak a csoportnak a neve, amely a tűzfalat tartalmazza.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Címke
A kulcs-érték párok a hash-táblázatok formájában. Példa:

@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetworkName
Annak a virtuális hálózatnak a neve, amelybe a tűzfalat telepíteni fogják. A virtuális hálózatnak és a tűzfalnak ugyanahhoz az erőforrás-csoporthoz kell tartoznia.

```yaml
Type: String
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
Type: SwitchParameter
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
Type: SwitchParameter
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
Ez a parancsmag nem fogadja el a bevitelt.

## KIMENETEK

### Microsoft. Azure. commands. Network. models. PSFirewall

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmFirewall](./Get-AzureRmFirewall.md)

[Remove-AzureRmFirewall](./Remove-AzureRmFirewall.md)

[Set-AzureRmFirewall](./Set-AzureRmFirewall.md)

[Új – AzureRmFirewallApplicationRuleCollection](./New-AzureRmFirewallApplicationRuleCollection.md)

[Új – AzureRmFirewallNatRuleCollection](./New-AzureRmFirewallNatRuleCollection.md)

[Új – AzureRmFirewallNetworkRuleCollection](./New-AzureRmFirewallNetworkRuleCollection.md)
