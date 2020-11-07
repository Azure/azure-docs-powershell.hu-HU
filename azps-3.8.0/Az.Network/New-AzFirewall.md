---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A3D60CF1-2E66-4EE5-9C68-932DD8DF80BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
ms.openlocfilehash: 3b4014b56a36228fe53221430ffe79a43118f8fe
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845009"
---
# New-AzFirewall

## Áttekintés
Új tűzfal létrehozása egy erőforrás-csoportban

## SZINTAXISA

### Alapértelmezett (alapértelmezett)
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String>
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-Zone <String[]>] [-Sku <String>] [-VirtualHubId <String>] [-FirewallPolicyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### OldIpConfigurationParameterValues
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetworkName <String>
 -PublicIpName <String> [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-Zone <String[]>] [-Sku <String>] [-VirtualHubId <String>] [-FirewallPolicyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### IpConfigurationParameterValues
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetwork <PSVirtualNetwork>
 -PublicIpAddress <PSPublicIpAddress[]> [-ManagementPublicIpAddress <PSPublicIpAddress>]
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-Zone <String[]>] [-Sku <String>] [-VirtualHubId <String>] [-FirewallPolicyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
A **New-AzFirewall** parancsmag Azure-tűzfalat hoz létre.

## Példák

### 1: virtuális hálózathoz kapcsolt tűzfal létrehozása
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip
```

Ez a példa létrehoz egy olyan tűzfalat, amely a "vnet" virtuális hálózathoz van csatolva a tűzfalban lévő erőforrás-csoportban.
Mivel nincs megadva szabály, a tűzfal letiltja az összes forgalmat (alapértelmezett viselkedés).
Az Intel veszélyforrás az alapértelmezett módban is fut – riasztás – ami azt jelenti, hogy a kártékony forgalom naplózva lesz, de nem tagadható meg.

### 2: tűzfal létrehozása, amely lehetővé teszi az összes HTTPS-forgalmat
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "https:443" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection
```

Ez a példa létrehoz egy tűzfalat, amely lehetővé teszi az összes HTTPS-forgalmat a 443-es porton keresztül.
Az Intel veszélyforrás az alapértelmezett módban fog futni – riasztás – ami azt jelenti, hogy a rendszer a kártékony forgalmat naplózza, de nem tagadja meg.

### 3: DNAT-átirányítja a forgalmat a 10.1.2.3:80 – 10.2.3.4:8080
```
$rule = New-AzFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.2.3.4" -TranslatedPort "8080"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "NatRuleCollection" -Priority 1000 -Rule $rule
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -NatRuleCollection $ruleCollection -ThreatIntelMode Off
```

Ez a példa létrehozta azt a tűzfalat, amely lefordította az 10.1.2.3-ra (80 – 10.2.3.4) irányuló összes csomag cél IP-portját: az 8080 veszélyforrás az Intel ki van kapcsolva ebben a példában.

### 4: szabály nélküli tűzfal létrehozása és az Intel veszélyforrása riasztás módban
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ThreatIntelMode Alert
```

Ez a példa létrehoz egy tűzfalat, amely blokkolja az összes forgalmat (az alapértelmezett viselkedést), és az Intel veszélyforrást jelenít meg riasztás módban.
Ez azt jelenti, hogy a rendszer riasztási naplókat bocsát ki a többi szabály alkalmazása előtt (ebben az esetben csak az alapértelmezett szabály: az összes elutasítása).

### 5: hozzon létre egy tűzfalat, amely lehetővé teszi az összes HTTP-forgalmat a 8080-on, de blokkolja az Intel által azonosított kártékony tartományokat.
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:8080" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

Ez a példa létrehoz egy tűzfalat, amely lehetővé teszi a 8080-on lévő összes HTTP-forgalom beállítását, kivéve, ha az Intel veszélyezteti az adatokat.
Ha a Megtagadás üzemmódban fut, az értesítéstől eltérően az Intel által kártékonynak tekintett forgalom nem csak a naplózás, hanem a blokkolás is.

### 6: szabály nélküli tűzfal létrehozása és elérhetőségi zónák
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetworkName $vnet.Name -PublicIpName $pip.Name -Zone 1,2,3
```

Ez a példa létrehoz egy tűzfalat az összes elérhető elérhetőségi zónával.

### 7: tűzfal létrehozása két vagy több nyilvános IP-címről
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -Name "vnet" -ResourceGroupName $rgName
$pip1 = New-AzPublicIpAddress -Name "AzFwPublicIp1" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$pip2 = New-AzPublicIpAddress -Name "AzFwPublicIp2" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress @($pip1, $pip2)
```

Ez a példa létrehoz egy "vnet" virtuális hálózathoz kapcsolt tűzfalat két nyilvános IP-címmel.

### 8: tűzfal létrehozása, amely lehetővé teszi az MSSQL-forgalom adott SQL-adatbázishoz való elérését
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "mssql:1433" -TargetFqdn "sql1.database.windows.net"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

Ebben a példában egy olyan tűzfal jön létre, amely lehetővé teszi az MSSQL-forgalomnak az 1433 standard porton való SQL-adatbázis sql1.database.windows.net.

### 9: virtuális hubhoz kapcsolt tűzfal létrehozása
```
$rgName = "resourceGroupName"
$fp = Get-AzFirewallPolicy -ResourceGroupName $rgName -Name "fp"
$fpId = $fp.Id
$vHub = Get-AzVirtualHub -Name "hub"
$vHubId = $vHub.Id

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -Sku AZFW_Hub -VirtualHubId $vHubId -FirewallPolicyId -$fpId
```

Ez a példa létrehoz egy tűzfalat, amely a Virtual hub "vHub" hivatkozással van társítva. Tűzfal-házirend $fp a tűzfalhoz. Ez a tűzfal engedélyezi/megtagadja a forgalmat a tűzfal házirend-$fpban említett szabályok alapján. A virtuális hub és a tűzfalnak ugyanabban a régióban kell lennie.

### 10: tűzfal létrehozása veszélyforrást tartalmazó intelligencia whitelist beállítással
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$tiWhitelist = New-AzFirewallThreatIntelWhitelist -FQDN @("www.microsoft.com") -IpAddresses @("8.8.8.8")
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ThreatIntelWhitelist $tiWhitelist
```

Ez a példa létrehoz egy tűzfalat, amely a "www.microsoft.com" és a "8.8.8.8" whitelist-ról a fenyegetések elleni intelligenciáról szól.

### 11: tűzfal létrehozása testreszabott privát tartománnyal beállítással
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -PrivateRange @("99.99.99.0/24", "66.66.0.0/16")
```

Ebben a példában egy olyan tűzfal jön létre, amely a "99.99.99.0/24" és a "66.66.0.0/16" privát IP-tartományokat kezeli, és nem SNAT a forgalmat a címekre

### 12: tűzfal létrehozása felügyeleti alhálózattal és nyilvános IP-címmel
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
$mgmtPip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "managementPublicIpName"

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ManagementPublicIpAddress $mgmtPip
```

Ez a példa létrehoz egy olyan tűzfalat, amely a "vnet" virtuális hálózathoz van csatolva a tűzfalban lévő erőforrás-csoportban.
Mivel nincs megadva szabály, a tűzfal letiltja az összes forgalmat (alapértelmezett viselkedés).
Az Intel veszélyforrás az alapértelmezett módban is fut – riasztás – ami azt jelenti, hogy a kártékony forgalom naplózva lesz, de nem tagadható meg.

A "kényszerített bújtatás" forgatókönyvek támogatása érdekében ez a tűzfal a "AzureFirewallManagementSubnet" alhálózatot fogja használni, és a felügyeleti központot a felügyeleti forgalomhoz tartozó nyilvános IP-címen

### 13: tűzfal létrehozása virtuális hálózathoz kapcsolódó tűzfal-házirenddel
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
$fp = Get-AzFirewallPolicy -ResourceGroupName $rgName -Name "fp"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -FirewallPolicyId $fp
```

Ez a példa létrehoz egy olyan tűzfalat, amely a "vnet" virtuális hálózathoz van csatolva a tűzfalban lévő erőforrás-csoportban.
A tűzfalra alkalmazott szabályok és veszélyforrások intelligencia a tűzfal házirendjében fog megjelenni.

## PARAMÉTEREK

### -ApplicationRuleCollection
Az új tűzfalhoz tartozó alkalmazási szabályok gyűjteményét adja meg.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection[]
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
Type: System.Management.Automation.SwitchParameter
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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FirewallPolicyId
A tűzfalhoz társított tűzfal-házirend

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

### -Force
Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.

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

### -Hely
A tűzfal régióját adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ManagementPublicIpAddress
Egy vagy több nyilvános IP-cím, amelyet a kezelési forgalomhoz szeretne használni. A nyilvános IP-címnek a standard SKU-nak kell lennie, és ugyanahhoz az erőforrás csoporthoz kell tartoznia, mint a tűzfalnak.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (név)
Annak az Azure-tűzfalnak a neve, amelyet a parancsmag hoz létre.

```yaml
Type: System.String
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
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection[]
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
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PrivateRange
Azok a privát IP-tartományok, amelyeken a forgalom nem lesz SNAT'ed

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

### -PublicIpAddress
Egy vagy több nyilvános IP-cím. A nyilvános IP-címnek a standard SKU-nak kell lennie, és ugyanahhoz az erőforrás csoporthoz kell tartoznia, mint a tűzfalnak.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress[]
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicIpName
Nyilvános IP-név. A nyilvános IP-nek a standard SKU-nak kell lennie, és ugyanahhoz az erőforrás csoporthoz kell tartoznia, mint a tűzfalnak.

```yaml
Type: System.String
Parameter Sets: OldIpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Annak a csoportnak a neve, amely a tűzfalat tartalmazza.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SKU
A tűzfal SKU-típusa

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AZFW_Hub, AZFW_VNet

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Címke
A kulcs-érték párok a hash-táblázatok formájában. Példa:

@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ThreatIntelMode
A veszélyforrások felderítésének működési módját adja meg. Az alapértelmezett üzemmód a riasztás, nem ki van kapcsolva.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Alert, Deny, Off

Required: False
Position: Named
Default value: Alert
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ThreatIntelWhitelist
A fenyegetések elleni intelligencia whitelist (whitelist)

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallThreatIntelWhitelist
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualHubId
A tűzfal által társított virtuális hub

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

### -VirtualNetwork
Virtuális hálózat

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VirtualNetworkName
Annak a virtuális hálózatnak a neve, amelybe a tűzfalat telepíteni fogják. A virtuális hálózatnak és a tűzfalnak ugyanahhoz az erőforrás-csoporthoz kell tartoznia.

```yaml
Type: System.String
Parameter Sets: OldIpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Zone (zóna)
Az elérhetőségi zónák listája, amely azt jelzi, hogy a tűzfalnak hol kell származnia.

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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

### Microsoft. Azure. commands. Network. models. PSVirtualNetwork

### Microsoft. Azure. commands. Network. models. PSPublicIpAddress []

### Microsoft. Azure. commands. Network. models. PSPublicIpAddress

### Microsoft. Azure. commands. Network. models. PSAzureFirewallApplicationRuleCollection []

### Microsoft. Azure. commands. Network. models. PSAzureFirewallNatRuleCollection []

### Microsoft. Azure. commands. Network. models. PSAzureFirewallNetworkRuleCollection []

### System. Collections. Hashtable

## KIMENETEK

### Microsoft. Azure. commands. Network. models. PSAzureFirewall

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzFirewall](./Get-AzFirewall.md)

[Remove-AzFirewall](./Remove-AzFirewall.md)

[Set-AzFirewall](./Set-AzFirewall.md)

[Új – AzFirewallApplicationRuleCollection](./New-AzFirewallApplicationRuleCollection.md)

[Új – AzFirewallNatRuleCollection](./New-AzFirewallNatRuleCollection.md)

[Új – AzFirewallNetworkRuleCollection](./New-AzFirewallNetworkRuleCollection.md)
