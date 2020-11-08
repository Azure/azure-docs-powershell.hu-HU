---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallnetworkrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRuleCollection.md
ms.openlocfilehash: 49a7484c0ca0b1a3dfa0feb82e09632d631333ed
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184844"
---
# <span data-ttu-id="a71ea-101">New-AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="a71ea-101">New-AzFirewallNetworkRuleCollection</span></span>

## <span data-ttu-id="a71ea-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a71ea-102">SYNOPSIS</span></span>
<span data-ttu-id="a71ea-103">Azure-tűzfal hálózati gyűjteményét hozza létre hálózati szabályokhoz.</span><span class="sxs-lookup"><span data-stu-id="a71ea-103">Creates a Azure Firewall Network Collection of Network rules.</span></span>

## <span data-ttu-id="a71ea-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a71ea-104">SYNTAX</span></span>

```
New-AzFirewallNetworkRuleCollection -Name <String> -Priority <UInt32> -Rule <PSAzureFirewallNetworkRule[]>
 -ActionType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a71ea-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a71ea-105">DESCRIPTION</span></span>
<span data-ttu-id="a71ea-106">A **New-AzFirewallNetworkRuleCollection** parancsmag tűzfal-hálózati szabályok gyűjteményét hozza létre.</span><span class="sxs-lookup"><span data-stu-id="a71ea-106">The **New-AzFirewallNetworkRuleCollection** cmdlet creates a collection of Firewall Network Rules.</span></span>

## <span data-ttu-id="a71ea-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a71ea-107">EXAMPLES</span></span>

### <span data-ttu-id="a71ea-108">1. példa: egy hálózati gyűjtemény létrehozása két szabállyal</span><span class="sxs-lookup"><span data-stu-id="a71ea-108">Example 1: Create a network collection with two rules</span></span>
```powershell
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$rule2 = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
New-AzFirewallNetworkRuleCollection -Name RC1 -Priority 100 -Rule $rule1, $rule2 -ActionType "Allow"
```

<span data-ttu-id="a71ea-109">Ez a példa olyan gyűjteményt hoz létre, amely lehetővé teszi az összes olyan adatforgalom beállítását, amely megfelel a két szabály egyikének.</span><span class="sxs-lookup"><span data-stu-id="a71ea-109">This example creates a collection which will allow all traffic that matches either of the two rules.</span></span>
<span data-ttu-id="a71ea-110">Az első szabály az összes UDP-forgalom esetén használható.</span><span class="sxs-lookup"><span data-stu-id="a71ea-110">The first rule is for all UDP traffic.</span></span>
<span data-ttu-id="a71ea-111">A második szabály a 10.0.0.0-től a 60.1.5.0-ig való TCP-forgalom: 4040.</span><span class="sxs-lookup"><span data-stu-id="a71ea-111">The second rule is for TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span>
<span data-ttu-id="a71ea-112">Ha létezik olyan hálózati szabály gyűjteménye, amely magasabb prioritással (kisebb számmal) rendelkezik, és a $rule 1 vagy $rule 2 értékben megjelölt forgalmat is megegyeznek, a magasabb prioritású szabály-gyűjteményben szereplő műveletek inkább az eredményben lépnek.</span><span class="sxs-lookup"><span data-stu-id="a71ea-112">If there is another Network rule collection with higher priority (smaller number) which also matches traffic identified in $rule1 or $rule2, the action of the rule collection with higher priority will take in effect instead.</span></span> 

### <span data-ttu-id="a71ea-113">2. példa: szabály hozzáadása egy szabály-gyűjteményhez</span><span class="sxs-lookup"><span data-stu-id="a71ea-113">Example 2: Add a rule to a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$ruleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"

$rule2 = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
$ruleCollection.AddRule($rule2)
```

<span data-ttu-id="a71ea-114">Ebben a példában egy új hálózati szabály-gyűjtemény jön létre egy szabállyal, majd egy második szabályt ad hozzá a szabályok gyűjteményéhez a szabály-gyűjtemény AddRule.</span><span class="sxs-lookup"><span data-stu-id="a71ea-114">This example creates a new network rule collection with one rule and then adds a second rule to the rule collection using method AddRule on the rule collection object.</span></span> <span data-ttu-id="a71ea-115">A megadott szabálygyűjtemény minden szabályának egyedi névvel kell rendelkeznie, és a kis-és nagybetűk megkülönböztetését is megadhatja.</span><span class="sxs-lookup"><span data-stu-id="a71ea-115">Each rule name in a given rule collection must have a unique name and is case insensitive.</span></span>

### <span data-ttu-id="a71ea-116">3. példa: szabály beszerzése egy szabály-gyűjteményből</span><span class="sxs-lookup"><span data-stu-id="a71ea-116">Example 3: Get a rule from a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$ruleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"
$getRule=$ruleCollection.GetRuleByName("ALL-UDP-traffic")
```

<span data-ttu-id="a71ea-117">Ebben a példában egy új hálózati szabály-gyűjtemény jön létre egy szabállyal, majd a szabályt név szerint, a hívási módszer GetRuleByName a szabály-gyűjtemény objektumon kapja.</span><span class="sxs-lookup"><span data-stu-id="a71ea-117">This example creates a new network rule collection with one rule and then gets the rule by name, calling method GetRuleByName on the rule collection object.</span></span> <span data-ttu-id="a71ea-118">A GetRuleByName metódus szabályának neve megkülönbözteti a kis-és nagybetűket.</span><span class="sxs-lookup"><span data-stu-id="a71ea-118">The rule name for method GetRuleByName is case-insensitive.</span></span>

### <span data-ttu-id="a71ea-119">4. példa: szabály eltávolítása egy szabály-gyűjteményből</span><span class="sxs-lookup"><span data-stu-id="a71ea-119">Example 4: Remove a rule from a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$rule2 = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
$ruleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1, $rule2 -ActionType "Allow"
$ruleCollection.RemoveRuleByName("ALL-udp-traffic")
```

<span data-ttu-id="a71ea-120">Ebben a példában egy új hálózati szabály-gyűjtemény jön létre két szabállyal, majd eltávolítja az első szabályt a szabály gyűjteményből a RemoveRuleByName metódust.</span><span class="sxs-lookup"><span data-stu-id="a71ea-120">This example creates a new network rule collection with two rules and then removes the first rule from the rule collection by calling method RemoveRuleByName on the rule collection object.</span></span> <span data-ttu-id="a71ea-121">A RemoveRuleByName metódus szabályának neve megkülönbözteti a kis-és nagybetűket.</span><span class="sxs-lookup"><span data-stu-id="a71ea-121">The rule name for method RemoveRuleByName is case-insensitive.</span></span>

## <span data-ttu-id="a71ea-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a71ea-122">PARAMETERS</span></span>

### <span data-ttu-id="a71ea-123">-ActionType</span><span class="sxs-lookup"><span data-stu-id="a71ea-123">-ActionType</span></span>
<span data-ttu-id="a71ea-124">Megadja, hogy milyen műveletek szükségesek a szabály forgalmi feltételeihez.</span><span class="sxs-lookup"><span data-stu-id="a71ea-124">Specifies the action to be taken for traffic matching conditions of this rule.</span></span> <span data-ttu-id="a71ea-125">Az elfogadott műveletek "Allow" vagy "deny".</span><span class="sxs-lookup"><span data-stu-id="a71ea-125">Accepted actions are "Allow" or "Deny".</span></span>

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

### <span data-ttu-id="a71ea-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a71ea-126">-DefaultProfile</span></span>
<span data-ttu-id="a71ea-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a71ea-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a71ea-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a71ea-128">-Name</span></span>
<span data-ttu-id="a71ea-129">A hálózati szabály-gyűjtemény nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a71ea-129">Specifies the name of this network rule collection.</span></span> <span data-ttu-id="a71ea-130">A névnek minden hálózati szabály-gyűjteményben egyedinek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="a71ea-130">The name must be unique across all network rule collection.</span></span>

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

### <span data-ttu-id="a71ea-131">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="a71ea-131">-Priority</span></span>
<span data-ttu-id="a71ea-132">A szabály-gyűjtemény prioritását adja meg.</span><span class="sxs-lookup"><span data-stu-id="a71ea-132">Specifies the priority of this rule collection.</span></span> <span data-ttu-id="a71ea-133">A prioritás az 100 és az 65000 közötti szám.</span><span class="sxs-lookup"><span data-stu-id="a71ea-133">Priority is a number between 100 and 65000.</span></span> <span data-ttu-id="a71ea-134">Minél kisebb a szám, annál nagyobb a prioritás.</span><span class="sxs-lookup"><span data-stu-id="a71ea-134">The smaller the number, the higher the priority.</span></span>

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

### <span data-ttu-id="a71ea-135">-Szabály</span><span class="sxs-lookup"><span data-stu-id="a71ea-135">-Rule</span></span>
<span data-ttu-id="a71ea-136">Az ebben a gyűjteményben csoportosítani kívánt szabályok listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="a71ea-136">Specifies the list of rules to be grouped under this collection.</span></span>

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

### <span data-ttu-id="a71ea-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a71ea-137">-Confirm</span></span>
<span data-ttu-id="a71ea-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a71ea-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a71ea-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a71ea-139">-WhatIf</span></span>
<span data-ttu-id="a71ea-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a71ea-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a71ea-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a71ea-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a71ea-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a71ea-142">CommonParameters</span></span>
<span data-ttu-id="a71ea-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a71ea-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a71ea-144">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a71ea-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a71ea-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a71ea-145">INPUTS</span></span>

### <span data-ttu-id="a71ea-146">Nincs</span><span class="sxs-lookup"><span data-stu-id="a71ea-146">None</span></span>

## <span data-ttu-id="a71ea-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a71ea-147">OUTPUTS</span></span>

### <span data-ttu-id="a71ea-148">Microsoft. Azure. commands. Network. models. PSAzureFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="a71ea-148">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection</span></span>

## <span data-ttu-id="a71ea-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a71ea-149">NOTES</span></span>

## <span data-ttu-id="a71ea-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a71ea-150">RELATED LINKS</span></span>

[<span data-ttu-id="a71ea-151">Új – AzFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="a71ea-151">New-AzFirewallNetworkRule</span></span>](./New-AzFirewallNetworkRule.md)

[<span data-ttu-id="a71ea-152">Új – AzFirewall</span><span class="sxs-lookup"><span data-stu-id="a71ea-152">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="a71ea-153">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="a71ea-153">Get-AzFirewall</span></span>](./Get-AzFirewall.md)