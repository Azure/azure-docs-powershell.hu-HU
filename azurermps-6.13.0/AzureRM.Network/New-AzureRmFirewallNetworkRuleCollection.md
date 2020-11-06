---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermfirewallnetworkrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallNetworkRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallNetworkRuleCollection.md
ms.openlocfilehash: 79ead5ac618b4631c3ec790156fe1a75e4169882
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498307"
---
# <span data-ttu-id="c5ebf-101">New-AzureRmFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="c5ebf-101">New-AzureRmFirewallNetworkRuleCollection</span></span>

## <span data-ttu-id="c5ebf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c5ebf-102">SYNOPSIS</span></span>
<span data-ttu-id="c5ebf-103">Azure-tűzfal hálózati gyűjteményét hozza létre hálózati szabályokhoz.</span><span class="sxs-lookup"><span data-stu-id="c5ebf-103">Creates a Azure Firewall Network Collection of Network rules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c5ebf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c5ebf-104">SYNTAX</span></span>

```
New-AzureRmFirewallNetworkRuleCollection -Name <String> -Priority <UInt32>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule]>
 -ActionType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5ebf-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c5ebf-105">DESCRIPTION</span></span>
<span data-ttu-id="c5ebf-106">A **New-AzureRmFirewallNetworkRuleCollection** parancsmag tűzfal-hálózati szabályok gyűjteményét hozza létre.</span><span class="sxs-lookup"><span data-stu-id="c5ebf-106">The **New-AzureRmFirewallNetworkRuleCollection** cmdlet creates a collection of Firewall Network Rules.</span></span>

## <span data-ttu-id="c5ebf-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c5ebf-107">EXAMPLES</span></span>

### <span data-ttu-id="c5ebf-108">1: egy hálózati gyűjtemény létrehozása két szabállyal</span><span class="sxs-lookup"><span data-stu-id="c5ebf-108">1:  Create a network collection with two rules</span></span>
```
$rule1 = New-AzureRmFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$rule2 = New-AzureRmFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
New-AzureRmFirewallNetworkRuleCollection -Name RC1 -Priority 100 -Rule $rule1, $rule2 -ActionType "Allow"
```

<span data-ttu-id="c5ebf-109">Ez a példa olyan gyűjteményt hoz létre, amely lehetővé teszi az összes olyan adatforgalom beállítását, amely megfelel a két szabály egyikének.</span><span class="sxs-lookup"><span data-stu-id="c5ebf-109">This example creates a collection which will allow all traffic that matches either of the two rules.</span></span>
<span data-ttu-id="c5ebf-110">Az első szabály az összes UDP-forgalom esetén használható.</span><span class="sxs-lookup"><span data-stu-id="c5ebf-110">The first rule is for all UDP traffic.</span></span>
<span data-ttu-id="c5ebf-111">A második szabály a 10.0.0.0-től a 60.1.5.0-ig való TCP-forgalom: 4040.</span><span class="sxs-lookup"><span data-stu-id="c5ebf-111">The second rule is for TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span>
<span data-ttu-id="c5ebf-112">Ha létezik olyan hálózati szabály gyűjteménye, amely magasabb prioritással (kisebb számmal) rendelkezik, és a $rule 1 vagy $rule 2 értékben megjelölt forgalmat is megegyeznek, a magasabb prioritású szabály-gyűjteményben szereplő műveletek inkább az eredményben lépnek.</span><span class="sxs-lookup"><span data-stu-id="c5ebf-112">If there is another Network rule collection with higher priority (smaller number) which also matches traffic identified in $rule1 or $rule2, the action of the rule collection with higher priority will take in effect instead.</span></span> 

### <span data-ttu-id="c5ebf-113">2: szabály hozzáadása egy szabály-gyűjteményhez</span><span class="sxs-lookup"><span data-stu-id="c5ebf-113">2:  Add a rule to a rule collection</span></span>
```
$rule1 = New-AzureRmFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$ruleCollection = New-AzureRmFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"

$rule2 = New-AzureRmFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
$ruleCollection.AddRule($rule2)
```

<span data-ttu-id="c5ebf-114">Ebben a példában egy új hálózati szabály-gyűjtemény jön létre egy szabállyal, majd egy második szabályt ad hozzá a szabályok gyűjteményéhez a szabály-gyűjtemény AddRule.</span><span class="sxs-lookup"><span data-stu-id="c5ebf-114">This example creates a new network rule collection with one rule and then adds a second rule to the rule collection using method AddRule on the rule collection object.</span></span> <span data-ttu-id="c5ebf-115">A megadott szabálygyűjtemény minden szabályának egyedi névvel kell rendelkeznie, és a kis-és nagybetűk megkülönböztetését is megadhatja.</span><span class="sxs-lookup"><span data-stu-id="c5ebf-115">Each rule name in a given rule collection must have a unique name and is case insensitive.</span></span>

### <span data-ttu-id="c5ebf-116">3: szabály kérése egy szabály-gyűjteményből</span><span class="sxs-lookup"><span data-stu-id="c5ebf-116">3:  Get a rule from a rule collection</span></span>
```
$rule1 = New-AzureRmFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$ruleCollection = New-AzureRmFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"
$getRule=$ruleCollection.GetRuleByName("ALL-UDP-traffic")
```

<span data-ttu-id="c5ebf-117">Ebben a példában egy új hálózati szabály-gyűjtemény jön létre egy szabállyal, majd a szabályt név szerint, a hívási módszer GetRuleByName a szabály-gyűjtemény objektumon kapja.</span><span class="sxs-lookup"><span data-stu-id="c5ebf-117">This example creates a new network rule collection with one rule and then gets the rule by name, calling method GetRuleByName on the rule collection object.</span></span> <span data-ttu-id="c5ebf-118">A GetRuleByName metódus szabályának neve megkülönbözteti a kis-és nagybetűket.</span><span class="sxs-lookup"><span data-stu-id="c5ebf-118">The rule name for method GetRuleByName is case-insensitive.</span></span>

### <span data-ttu-id="c5ebf-119">4: szabály eltávolítása a szabályok gyűjteményéből</span><span class="sxs-lookup"><span data-stu-id="c5ebf-119">4:  Remove a rule from a rule collection</span></span>
```
$rule1 = New-AzureRmFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$rule2 = New-AzureRmFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
$ruleCollection = New-AzureRmFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1, $rule2 -ActionType "Allow"
$ruleCollection.RemoveRuleByName("ALL-udp-traffic")
```

<span data-ttu-id="c5ebf-120">Ebben a példában egy új hálózati szabály-gyűjtemény jön létre két szabállyal, majd eltávolítja az első szabályt a szabály gyűjteményből a RemoveRuleByName metódust.</span><span class="sxs-lookup"><span data-stu-id="c5ebf-120">This example creates a new network rule collection with two rules and then removes the first rule from the rule collection by calling method RemoveRuleByName on the rule collection object.</span></span> <span data-ttu-id="c5ebf-121">A RemoveRuleByName metódus szabályának neve megkülönbözteti a kis-és nagybetűket.</span><span class="sxs-lookup"><span data-stu-id="c5ebf-121">The rule name for method RemoveRuleByName is case-insensitive.</span></span>

## <span data-ttu-id="c5ebf-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c5ebf-122">PARAMETERS</span></span>

### <span data-ttu-id="c5ebf-123">-ActionType</span><span class="sxs-lookup"><span data-stu-id="c5ebf-123">-ActionType</span></span>
<span data-ttu-id="c5ebf-124">Megadja, hogy milyen műveletek szükségesek a szabály forgalmi feltételeihez.</span><span class="sxs-lookup"><span data-stu-id="c5ebf-124">Specifies the action to be taken for traffic matching conditions of this rule.</span></span> <span data-ttu-id="c5ebf-125">Az elfogadott műveletek "Allow" vagy "deny".</span><span class="sxs-lookup"><span data-stu-id="c5ebf-125">Accepted actions are "Allow" or "Deny".</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5ebf-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5ebf-126">-DefaultProfile</span></span>
<span data-ttu-id="c5ebf-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c5ebf-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5ebf-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c5ebf-128">-Name</span></span>
<span data-ttu-id="c5ebf-129">A hálózati szabály-gyűjtemény nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c5ebf-129">Specifies the name of this network rule collection.</span></span> <span data-ttu-id="c5ebf-130">A névnek minden hálózati szabály-gyűjteményben egyedinek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="c5ebf-130">The name must be unique across all network rule collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5ebf-131">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="c5ebf-131">-Priority</span></span>
<span data-ttu-id="c5ebf-132">A szabály-gyűjtemény prioritását adja meg.</span><span class="sxs-lookup"><span data-stu-id="c5ebf-132">Specifies the priority of this rule collection.</span></span> <span data-ttu-id="c5ebf-133">A prioritás az 100 és az 65000 közötti szám.</span><span class="sxs-lookup"><span data-stu-id="c5ebf-133">Priority is a number between 100 and 65000.</span></span> <span data-ttu-id="c5ebf-134">Minél kisebb a szám, annál nagyobb a prioritás.</span><span class="sxs-lookup"><span data-stu-id="c5ebf-134">The smaller the number, the higher the priority.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5ebf-135">-Szabály</span><span class="sxs-lookup"><span data-stu-id="c5ebf-135">-Rule</span></span>
<span data-ttu-id="c5ebf-136">Az ebben a gyűjteményben csoportosítani kívánt szabályok listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c5ebf-136">Specifies the list of rules to be grouped under this collection.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5ebf-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c5ebf-137">-Confirm</span></span>
<span data-ttu-id="c5ebf-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c5ebf-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5ebf-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5ebf-139">-WhatIf</span></span>
<span data-ttu-id="c5ebf-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c5ebf-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5ebf-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c5ebf-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5ebf-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5ebf-142">CommonParameters</span></span>
<span data-ttu-id="c5ebf-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c5ebf-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5ebf-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5ebf-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5ebf-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c5ebf-145">INPUTS</span></span>

### <span data-ttu-id="c5ebf-146">Nincs</span><span class="sxs-lookup"><span data-stu-id="c5ebf-146">None</span></span>
<span data-ttu-id="c5ebf-147">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="c5ebf-147">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c5ebf-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c5ebf-148">OUTPUTS</span></span>

### <span data-ttu-id="c5ebf-149">Microsoft. Azure. commands. Network. models. PSFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="c5ebf-149">Microsoft.Azure.Commands.Network.Models.PSFirewallNetworkRuleCollection</span></span>

## <span data-ttu-id="c5ebf-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c5ebf-150">NOTES</span></span>

## <span data-ttu-id="c5ebf-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c5ebf-151">RELATED LINKS</span></span>

[<span data-ttu-id="c5ebf-152">Új – AzureRmFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="c5ebf-152">New-AzureRmFirewallNetworkRule</span></span>](./New-AzureRmFirewallNetworkRule.md)

[<span data-ttu-id="c5ebf-153">Új – AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="c5ebf-153">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)

[<span data-ttu-id="c5ebf-154">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="c5ebf-154">Get-AzureRmFirewall</span></span>](./Get-AzureRmFirewall.md)
