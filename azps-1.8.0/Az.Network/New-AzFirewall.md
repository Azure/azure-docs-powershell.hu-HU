---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A3D60CF1-2E66-4EE5-9C68-932DD8DF80BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
ms.openlocfilehash: 48e8fc8685073a0fad742152191fe68c368fbb3f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670345"
---
# <span data-ttu-id="db874-101">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="db874-101">New-AzFirewall</span></span>

## <span data-ttu-id="db874-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="db874-102">SYNOPSIS</span></span>
<span data-ttu-id="db874-103">Új tűzfal létrehozása egy erőforrás-csoportban</span><span class="sxs-lookup"><span data-stu-id="db874-103">Creates a new Firewall in a resource group.</span></span>

## <span data-ttu-id="db874-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="db874-104">SYNTAX</span></span>

### <span data-ttu-id="db874-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="db874-105">Default (Default)</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String>
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db874-106">IpConfigurationParameterValues</span><span class="sxs-lookup"><span data-stu-id="db874-106">IpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetworkName <String>
 -PublicIpName <String> [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db874-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="db874-107">DESCRIPTION</span></span>
<span data-ttu-id="db874-108">A **New-AzFirewall** parancsmag Azure-tűzfalat hoz létre.</span><span class="sxs-lookup"><span data-stu-id="db874-108">The **New-AzFirewall** cmdlet creates an Azure Firewall.</span></span>

## <span data-ttu-id="db874-109">Példák</span><span class="sxs-lookup"><span data-stu-id="db874-109">EXAMPLES</span></span>

### <span data-ttu-id="db874-110">1: virtuális hálózathoz kapcsolt tűzfal létrehozása</span><span class="sxs-lookup"><span data-stu-id="db874-110">1:  Create a Firewall attached to a virtual network</span></span>
```
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -VirtualNetworkName "vnet" -PublicIpName "pip-name"
```

<span data-ttu-id="db874-111">Ez a példa létrehoz egy olyan tűzfalat, amely a "vnet" virtuális hálózathoz van csatolva a tűzfalban lévő erőforrás-csoportban.</span><span class="sxs-lookup"><span data-stu-id="db874-111">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="db874-112">Mivel nincs megadva szabály, a tűzfal letiltja az összes forgalmat (alapértelmezett viselkedés).</span><span class="sxs-lookup"><span data-stu-id="db874-112">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>
<span data-ttu-id="db874-113">Az Intel veszélyforrás az alapértelmezett módban is fut – riasztás – ami azt jelenti, hogy a kártékony forgalom naplózva lesz, de nem tagadható meg.</span><span class="sxs-lookup"><span data-stu-id="db874-113">Threat Intel will also run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="db874-114">2: tűzfal létrehozása, amely lehetővé teszi az összes HTTPS-forgalmat</span><span class="sxs-lookup"><span data-stu-id="db874-114">2:  Create a Firewall which allows all HTTPS traffic</span></span>
```
$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "https:443" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -VirtualNetworkName "vnet" -PublicIpName "pip-name" -ApplicationRuleCollection $ruleCollection
```

<span data-ttu-id="db874-115">Ez a példa létrehoz egy tűzfalat, amely lehetővé teszi az összes HTTPS-forgalmat a 443-es porton keresztül.</span><span class="sxs-lookup"><span data-stu-id="db874-115">This example creates a Firewall which allows all HTTPS traffic on port 443.</span></span>
<span data-ttu-id="db874-116">Az Intel veszélyforrás az alapértelmezett módban fog futni – riasztás – ami azt jelenti, hogy a rendszer a kártékony forgalmat naplózza, de nem tagadja meg.</span><span class="sxs-lookup"><span data-stu-id="db874-116">Threat Intel will run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="db874-117">3: DNAT-átirányítja a forgalmat a 10.1.2.3:80 – 10.2.3.4:8080</span><span class="sxs-lookup"><span data-stu-id="db874-117">3:  DNAT - redirect traffic destined to 10.1.2.3:80 to 10.2.3.4:8080</span></span>
```
$rule = New-AzFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.2.3.4" -TranslatedPort "8080"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "NatRuleCollection" -Priority 1000 -Rule $rule
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -NatRuleCollection $ruleCollection -ThreatIntelMode Off
```

<span data-ttu-id="db874-118">Ez a példa létrehozta azt a tűzfalat, amely lefordította az 10.1.2.3-ra (80 – 10.2.3.4) irányuló összes csomag cél IP-portját: az 8080 veszélyforrás az Intel ki van kapcsolva ebben a példában.</span><span class="sxs-lookup"><span data-stu-id="db874-118">This example created a Firewall which translated the destination IP and port of all packets destined to 10.1.2.3:80 to 10.2.3.4:8080 Threat Intel is turned off in this example.</span></span>

### <span data-ttu-id="db874-119">4: szabály nélküli tűzfal létrehozása és az Intel veszélyforrása riasztás módban</span><span class="sxs-lookup"><span data-stu-id="db874-119">4:  Create a Firewall with no rules and with Threat Intel in Alert mode</span></span>
```
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -VirtualNetworkName "vnet" -PublicIpName "pip-name" -ThreatIntelMode Alert
```

<span data-ttu-id="db874-120">Ez a példa létrehoz egy tűzfalat, amely blokkolja az összes forgalmat (az alapértelmezett viselkedést), és az Intel veszélyforrást jelenít meg riasztás módban.</span><span class="sxs-lookup"><span data-stu-id="db874-120">This example creates a Firewall which blocks all traffic (default behavior) and has Threat Intel running in Alert mode.</span></span>
<span data-ttu-id="db874-121">Ez azt jelenti, hogy a rendszer riasztási naplókat bocsát ki a többi szabály alkalmazása előtt (ebben az esetben csak az alapértelmezett szabály: az összes elutasítása).</span><span class="sxs-lookup"><span data-stu-id="db874-121">This means alerting logs are emitted for malicious traffic before applying the other rules (in this case just the default rule - Deny All)</span></span>

### <span data-ttu-id="db874-122">5: hozzon létre egy tűzfalat, amely lehetővé teszi az összes HTTP-forgalmat a 8080-on, de blokkolja az Intel által azonosított kártékony tartományokat.</span><span class="sxs-lookup"><span data-stu-id="db874-122">5:  Create a Firewall which allows all HTTP traffic on port 8080, but blocks malicious domains identified by Threat Intel</span></span>
```
$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:8080" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -VirtualNetworkName "vnet" -PublicIpName "pip-name" -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="db874-123">Ez a példa létrehoz egy tűzfalat, amely lehetővé teszi a 8080-on lévő összes HTTP-forgalom beállítását, kivéve, ha az Intel veszélyezteti az adatokat.</span><span class="sxs-lookup"><span data-stu-id="db874-123">This example creates a Firewall which allows all HTTP traffic on port 8080 unless it is considered malicious by Threat Intel.</span></span>
<span data-ttu-id="db874-124">Ha a Megtagadás üzemmódban fut, az értesítéstől eltérően az Intel által kártékonynak tekintett forgalom nem csak a naplózás, hanem a blokkolás is.</span><span class="sxs-lookup"><span data-stu-id="db874-124">When running in Deny mode, unlike Alert, traffic considered malicious by Threat Intel is not just logged, but also blocked.</span></span>

## <span data-ttu-id="db874-125">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="db874-125">PARAMETERS</span></span>

### <span data-ttu-id="db874-126">-ApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="db874-126">-ApplicationRuleCollection</span></span>
<span data-ttu-id="db874-127">Az új tűzfalhoz tartozó alkalmazási szabályok gyűjteményét adja meg.</span><span class="sxs-lookup"><span data-stu-id="db874-127">Specifies the collections of application rules for the new Firewall.</span></span>

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

### <span data-ttu-id="db874-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="db874-128">-AsJob</span></span>
<span data-ttu-id="db874-129">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="db874-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="db874-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db874-130">-DefaultProfile</span></span>
<span data-ttu-id="db874-131">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="db874-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db874-132">-Force</span><span class="sxs-lookup"><span data-stu-id="db874-132">-Force</span></span>
<span data-ttu-id="db874-133">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="db874-133">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="db874-134">-Hely</span><span class="sxs-lookup"><span data-stu-id="db874-134">-Location</span></span>
<span data-ttu-id="db874-135">A tűzfal régióját adja meg.</span><span class="sxs-lookup"><span data-stu-id="db874-135">Specifies the region for the Firewall.</span></span>

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

### <span data-ttu-id="db874-136">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="db874-136">-Name</span></span>
<span data-ttu-id="db874-137">Annak az Azure-tűzfalnak a neve, amelyet a parancsmag hoz létre.</span><span class="sxs-lookup"><span data-stu-id="db874-137">Specifies the name of the Azure Firewall that this cmdlet creates.</span></span>

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

### <span data-ttu-id="db874-138">-NatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="db874-138">-NatRuleCollection</span></span>
<span data-ttu-id="db874-139">A AzureFirewallNatRuleCollections listája</span><span class="sxs-lookup"><span data-stu-id="db874-139">The list of AzureFirewallNatRuleCollections</span></span>

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

### <span data-ttu-id="db874-140">-NetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="db874-140">-NetworkRuleCollection</span></span>
<span data-ttu-id="db874-141">A AzureFirewallNetworkRuleCollections listája</span><span class="sxs-lookup"><span data-stu-id="db874-141">The list of AzureFirewallNetworkRuleCollections</span></span>

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

### <span data-ttu-id="db874-142">-PublicIpName</span><span class="sxs-lookup"><span data-stu-id="db874-142">-PublicIpName</span></span>
<span data-ttu-id="db874-143">Nyilvános IP-név.</span><span class="sxs-lookup"><span data-stu-id="db874-143">Public Ip Name.</span></span> <span data-ttu-id="db874-144">A nyilvános IP-nek a standard SKU-nak kell lennie, és ugyanahhoz az erőforrás csoporthoz kell tartoznia, mint a tűzfalnak.</span><span class="sxs-lookup"><span data-stu-id="db874-144">The Public IP must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

```yaml
Type: System.String
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db874-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db874-145">-ResourceGroupName</span></span>
<span data-ttu-id="db874-146">Annak a csoportnak a neve, amely a tűzfalat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="db874-146">Specifies the name of a resource group to contain the Firewall.</span></span>

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

### <span data-ttu-id="db874-147">-Címke</span><span class="sxs-lookup"><span data-stu-id="db874-147">-Tag</span></span>
<span data-ttu-id="db874-148">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="db874-148">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="db874-149">Példa:</span><span class="sxs-lookup"><span data-stu-id="db874-149">For example:</span></span>

<span data-ttu-id="db874-150">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="db874-150">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="db874-151">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="db874-151">-ThreatIntelMode</span></span>
<span data-ttu-id="db874-152">A veszélyforrások felderítésének működési módját adja meg.</span><span class="sxs-lookup"><span data-stu-id="db874-152">Specifies the operation mode for Threat Intelligence.</span></span> <span data-ttu-id="db874-153">Az alapértelmezett üzemmód a riasztás, nem ki van kapcsolva.</span><span class="sxs-lookup"><span data-stu-id="db874-153">Default mode is Alert, not Off.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Alert
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db874-154">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="db874-154">-VirtualNetworkName</span></span>
<span data-ttu-id="db874-155">Annak a virtuális hálózatnak a neve, amelybe a tűzfalat telepíteni fogják.</span><span class="sxs-lookup"><span data-stu-id="db874-155">Specifies the name of the virtual network for which the Firewall will be deployed.</span></span> <span data-ttu-id="db874-156">A virtuális hálózatnak és a tűzfalnak ugyanahhoz az erőforrás-csoporthoz kell tartoznia.</span><span class="sxs-lookup"><span data-stu-id="db874-156">Virtual network and Firewall must belong to the same resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db874-157">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="db874-157">-Confirm</span></span>
<span data-ttu-id="db874-158">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="db874-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db874-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db874-159">-WhatIf</span></span>
<span data-ttu-id="db874-160">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="db874-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db874-161">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="db874-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db874-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db874-162">CommonParameters</span></span>
<span data-ttu-id="db874-163">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="db874-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db874-164">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db874-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db874-165">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="db874-165">INPUTS</span></span>

### <span data-ttu-id="db874-166">System. String</span><span class="sxs-lookup"><span data-stu-id="db874-166">System.String</span></span>

### <span data-ttu-id="db874-167">Microsoft. Azure. commands. Network. models. PSAzureFirewallApplicationRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="db874-167">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection[]</span></span>

### <span data-ttu-id="db874-168">Microsoft. Azure. commands. Network. models. PSAzureFirewallNatRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="db874-168">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection[]</span></span>

### <span data-ttu-id="db874-169">Microsoft. Azure. commands. Network. models. PSAzureFirewallNetworkRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="db874-169">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection[]</span></span>

### <span data-ttu-id="db874-170">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="db874-170">System.Collections.Hashtable</span></span>

## <span data-ttu-id="db874-171">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="db874-171">OUTPUTS</span></span>

### <span data-ttu-id="db874-172">Microsoft. Azure. commands. Network. models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="db874-172">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="db874-173">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="db874-173">NOTES</span></span>

## <span data-ttu-id="db874-174">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="db874-174">RELATED LINKS</span></span>

[<span data-ttu-id="db874-175">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="db874-175">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="db874-176">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="db874-176">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)

[<span data-ttu-id="db874-177">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="db874-177">Set-AzFirewall</span></span>](./Set-AzFirewall.md)

[<span data-ttu-id="db874-178">Új – AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="db874-178">New-AzFirewallApplicationRuleCollection</span></span>](./New-AzFirewallApplicationRuleCollection.md)

[<span data-ttu-id="db874-179">Új – AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="db874-179">New-AzFirewallNatRuleCollection</span></span>](./New-AzFirewallNatRuleCollection.md)

[<span data-ttu-id="db874-180">Új – AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="db874-180">New-AzFirewallNetworkRuleCollection</span></span>](./New-AzFirewallNetworkRuleCollection.md)
