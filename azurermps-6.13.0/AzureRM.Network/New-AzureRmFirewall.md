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
# <span data-ttu-id="9e557-101">New-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="9e557-101">New-AzureRmFirewall</span></span>

## <span data-ttu-id="9e557-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9e557-102">SYNOPSIS</span></span>
<span data-ttu-id="9e557-103">Új tűzfal létrehozása egy erőforrás-csoportban</span><span class="sxs-lookup"><span data-stu-id="9e557-103">Creates a new Firewall in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e557-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9e557-104">SYNTAX</span></span>

```
New-AzureRmFirewall -Name <String> -ResourceGroupName <String> -Location <String>
 [-VirtualNetworkName <String>] [-PublicIpName <String>]
 [-ApplicationRuleCollection <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection]>]
 [-NatRuleCollection <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection]>]
 [-NetworkRuleCollection <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9e557-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9e557-105">DESCRIPTION</span></span>
<span data-ttu-id="9e557-106">A **New-AzureRmFirewall** parancsmag Azure-tűzfalat hoz létre.</span><span class="sxs-lookup"><span data-stu-id="9e557-106">The **New-AzureRmFirewall** cmdlet creates an Azure Firewall.</span></span>

## <span data-ttu-id="9e557-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9e557-107">EXAMPLES</span></span>

### <span data-ttu-id="9e557-108">1: virtuális hálózathoz kapcsolt tűzfal létrehozása</span><span class="sxs-lookup"><span data-stu-id="9e557-108">1:  Create a Firewall attached to a virtual network</span></span>
```
New-AzureRmFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -VirtualNetworkName "vnet" -PublicIpName "pip-name"
```

<span data-ttu-id="9e557-109">Ez a példa létrehoz egy olyan tűzfalat, amely a "vnet" virtuális hálózathoz van csatolva a tűzfalban lévő erőforrás-csoportban.</span><span class="sxs-lookup"><span data-stu-id="9e557-109">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="9e557-110">Mivel nincs megadva szabály, a tűzfal letiltja az összes forgalmat (alapértelmezett viselkedés).</span><span class="sxs-lookup"><span data-stu-id="9e557-110">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>

### <span data-ttu-id="9e557-111">2: tűzfal létrehozása, amely lehetővé teszi az összes HTTPS-forgalmat</span><span class="sxs-lookup"><span data-stu-id="9e557-111">2:  Create a Firewall which allows all HTTPS traffic</span></span>
```
$rule = New-AzureRmFirewallApplicationRule -Name R1 -Protocol "https:443" -TargetFqdn "*" 
$ruleCollection = New-AzureRmFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzureRmFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -VirtualNetworkName "vnet" -PublicIpName "pip-name" -ApplicationRuleCollection $ruleCollection
```

<span data-ttu-id="9e557-112">Ez a példa létrehoz egy tűzfalat, amely lehetővé teszi az összes HTTPS-forgalmat a 443-es porton keresztül.</span><span class="sxs-lookup"><span data-stu-id="9e557-112">This example creates a Firewall which allows all HTTPS traffic on port 443.</span></span>

### <span data-ttu-id="9e557-113">3: DNAT-átirányítja a forgalmat a 10.1.2.3:80 – 10.2.3.4:8080</span><span class="sxs-lookup"><span data-stu-id="9e557-113">3:  DNAT - redirect traffic destined to 10.1.2.3:80 to 10.2.3.4:8080</span></span>
```
$rule = New-AzureRmFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.2.3.4" -TranslatedPort "8080"
$ruleCollection = New-AzureRmFirewallNatRuleCollection -Name "NatRuleCollection" -Priority 1000 -Rule $rule
New-AzureRmFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -NatRuleCollection $ruleCollection
```

<span data-ttu-id="9e557-114">Ez a példa létrehozta azt a tűzfalat, amely lefordította az 10.1.2.3-ra szánt összes csomag cél IP-címe és portja: 10.2.3.4:8080</span><span class="sxs-lookup"><span data-stu-id="9e557-114">This example created a Firewall which translated the destination IP and port of all packets destined to 10.1.2.3:80 to 10.2.3.4:8080</span></span>

## <span data-ttu-id="9e557-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9e557-115">PARAMETERS</span></span>

### <span data-ttu-id="9e557-116">-ApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="9e557-116">-ApplicationRuleCollection</span></span>
<span data-ttu-id="9e557-117">Az új tűzfalhoz tartozó alkalmazási szabályok gyűjteményét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9e557-117">Specifies the collections of application rules for the new Firewall.</span></span>

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

### <span data-ttu-id="9e557-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9e557-118">-AsJob</span></span>
<span data-ttu-id="9e557-119">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="9e557-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9e557-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e557-120">-DefaultProfile</span></span>
<span data-ttu-id="9e557-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9e557-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e557-122">-Force</span><span class="sxs-lookup"><span data-stu-id="9e557-122">-Force</span></span>
<span data-ttu-id="9e557-123">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="9e557-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9e557-124">-Hely</span><span class="sxs-lookup"><span data-stu-id="9e557-124">-Location</span></span>
<span data-ttu-id="9e557-125">A tűzfal régióját adja meg.</span><span class="sxs-lookup"><span data-stu-id="9e557-125">Specifies the region for the Firewall.</span></span>

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

### <span data-ttu-id="9e557-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9e557-126">-Name</span></span>
<span data-ttu-id="9e557-127">Annak az Azure-tűzfalnak a neve, amelyet a parancsmag hoz létre.</span><span class="sxs-lookup"><span data-stu-id="9e557-127">Specifies the name of the Azure Firewall that this cmdlet creates.</span></span>

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

### <span data-ttu-id="9e557-128">-NatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="9e557-128">-NatRuleCollection</span></span>
<span data-ttu-id="9e557-129">A AzureFirewallNatRuleCollections listája</span><span class="sxs-lookup"><span data-stu-id="9e557-129">The list of AzureFirewallNatRuleCollections</span></span>

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

### <span data-ttu-id="9e557-130">-NetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="9e557-130">-NetworkRuleCollection</span></span>
<span data-ttu-id="9e557-131">A AzureFirewallNetworkRuleCollections listája</span><span class="sxs-lookup"><span data-stu-id="9e557-131">The list of AzureFirewallNetworkRuleCollections</span></span>

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

### <span data-ttu-id="9e557-132">-PublicIpName</span><span class="sxs-lookup"><span data-stu-id="9e557-132">-PublicIpName</span></span>
<span data-ttu-id="9e557-133">Nyilvános IP-név.</span><span class="sxs-lookup"><span data-stu-id="9e557-133">Public Ip Name.</span></span> <span data-ttu-id="9e557-134">A nyilvános IP-nek a standard SKU-nak kell lennie, és ugyanahhoz az erőforrás csoporthoz kell tartoznia, mint a tűzfalnak.</span><span class="sxs-lookup"><span data-stu-id="9e557-134">The Public IP must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

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

### <span data-ttu-id="9e557-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e557-135">-ResourceGroupName</span></span>
<span data-ttu-id="9e557-136">Annak a csoportnak a neve, amely a tűzfalat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="9e557-136">Specifies the name of a resource group to contain the Firewall.</span></span>

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

### <span data-ttu-id="9e557-137">-Címke</span><span class="sxs-lookup"><span data-stu-id="9e557-137">-Tag</span></span>
<span data-ttu-id="9e557-138">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="9e557-138">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="9e557-139">Példa:</span><span class="sxs-lookup"><span data-stu-id="9e557-139">For example:</span></span>

<span data-ttu-id="9e557-140">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="9e557-140">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="9e557-141">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="9e557-141">-VirtualNetworkName</span></span>
<span data-ttu-id="9e557-142">Annak a virtuális hálózatnak a neve, amelybe a tűzfalat telepíteni fogják.</span><span class="sxs-lookup"><span data-stu-id="9e557-142">Specifies the name of the virtual network for which the Firewall will be deployed.</span></span> <span data-ttu-id="9e557-143">A virtuális hálózatnak és a tűzfalnak ugyanahhoz az erőforrás-csoporthoz kell tartoznia.</span><span class="sxs-lookup"><span data-stu-id="9e557-143">Virtual network and Firewall must belong to the same resource group.</span></span>

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

### <span data-ttu-id="9e557-144">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9e557-144">-Confirm</span></span>
<span data-ttu-id="9e557-145">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9e557-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e557-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e557-146">-WhatIf</span></span>
<span data-ttu-id="9e557-147">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9e557-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e557-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9e557-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e557-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e557-149">CommonParameters</span></span>
<span data-ttu-id="9e557-150">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9e557-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e557-151">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e557-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e557-152">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9e557-152">INPUTS</span></span>

### <span data-ttu-id="9e557-153">Nincs</span><span class="sxs-lookup"><span data-stu-id="9e557-153">None</span></span>
<span data-ttu-id="9e557-154">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="9e557-154">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9e557-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9e557-155">OUTPUTS</span></span>

### <span data-ttu-id="9e557-156">Microsoft. Azure. commands. Network. models. PSFirewall</span><span class="sxs-lookup"><span data-stu-id="9e557-156">Microsoft.Azure.Commands.Network.Models.PSFirewall</span></span>

## <span data-ttu-id="9e557-157">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9e557-157">NOTES</span></span>

## <span data-ttu-id="9e557-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9e557-158">RELATED LINKS</span></span>

[<span data-ttu-id="9e557-159">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="9e557-159">Get-AzureRmFirewall</span></span>](./Get-AzureRmFirewall.md)

[<span data-ttu-id="9e557-160">Remove-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="9e557-160">Remove-AzureRmFirewall</span></span>](./Remove-AzureRmFirewall.md)

[<span data-ttu-id="9e557-161">Set-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="9e557-161">Set-AzureRmFirewall</span></span>](./Set-AzureRmFirewall.md)

[<span data-ttu-id="9e557-162">Új – AzureRmFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="9e557-162">New-AzureRmFirewallApplicationRuleCollection</span></span>](./New-AzureRmFirewallApplicationRuleCollection.md)

[<span data-ttu-id="9e557-163">Új – AzureRmFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="9e557-163">New-AzureRmFirewallNatRuleCollection</span></span>](./New-AzureRmFirewallNatRuleCollection.md)

[<span data-ttu-id="9e557-164">Új – AzureRmFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="9e557-164">New-AzureRmFirewallNetworkRuleCollection</span></span>](./New-AzureRmFirewallNetworkRuleCollection.md)
