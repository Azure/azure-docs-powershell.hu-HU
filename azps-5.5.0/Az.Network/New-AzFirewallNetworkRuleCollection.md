---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallnetworkrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRuleCollection.md
ms.openlocfilehash: 49a7484c0ca0b1a3dfa0feb82e09632d631333ed
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206734"
---
# <span data-ttu-id="4fce5-101">New-AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="4fce5-101">New-AzFirewallNetworkRuleCollection</span></span>

## <span data-ttu-id="4fce5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4fce5-102">SYNOPSIS</span></span>
<span data-ttu-id="4fce5-103">Létrehozza az Azure Firewall Network Network Collection of Network rules (Hálózati szabályok) gyűjteményt.</span><span class="sxs-lookup"><span data-stu-id="4fce5-103">Creates a Azure Firewall Network Collection of Network rules.</span></span>

## <span data-ttu-id="4fce5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4fce5-104">SYNTAX</span></span>

```
New-AzFirewallNetworkRuleCollection -Name <String> -Priority <UInt32> -Rule <PSAzureFirewallNetworkRule[]>
 -ActionType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4fce5-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4fce5-105">DESCRIPTION</span></span>
<span data-ttu-id="4fce5-106">A **New-AzFirewallNetworkRuleCollection** parancsmag tűzfalhálózati szabályok gyűjteményét hozza létre.</span><span class="sxs-lookup"><span data-stu-id="4fce5-106">The **New-AzFirewallNetworkRuleCollection** cmdlet creates a collection of Firewall Network Rules.</span></span>

## <span data-ttu-id="4fce5-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4fce5-107">EXAMPLES</span></span>

### <span data-ttu-id="4fce5-108">1. példa: Két szabályokkal létrehozott hálózati gyűjtemény</span><span class="sxs-lookup"><span data-stu-id="4fce5-108">Example 1: Create a network collection with two rules</span></span>
```powershell
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$rule2 = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
New-AzFirewallNetworkRuleCollection -Name RC1 -Priority 100 -Rule $rule1, $rule2 -ActionType "Allow"
```

<span data-ttu-id="4fce5-109">Ez a példa létrehoz egy gyűjteményt, amely engedélyezi a két szabály bármelyikének megfelelő forgalmat.</span><span class="sxs-lookup"><span data-stu-id="4fce5-109">This example creates a collection which will allow all traffic that matches either of the two rules.</span></span>
<span data-ttu-id="4fce5-110">Az első szabály az összes UDP-forgalomra vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="4fce5-110">The first rule is for all UDP traffic.</span></span>
<span data-ttu-id="4fce5-111">A második szabály a 10.0.0.0 és 60.1.5.0:4040-es TCP-forgalomra vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="4fce5-111">The second rule is for TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span>
<span data-ttu-id="4fce5-112">Ha egy másik, magasabb prioritású (kisebb számú) szabálygyűjtemény is van, amely az $rule 1-ben vagy a $rule 2-ben azonosított forgalommal is egyezik, akkor a magasabb prioritású szabálygyűjteményre vonatkozó művelet lép életbe.</span><span class="sxs-lookup"><span data-stu-id="4fce5-112">If there is another Network rule collection with higher priority (smaller number) which also matches traffic identified in $rule1 or $rule2, the action of the rule collection with higher priority will take in effect instead.</span></span> 

### <span data-ttu-id="4fce5-113">2. példa: Szabály hozzáadása szabálygyűjteményhez</span><span class="sxs-lookup"><span data-stu-id="4fce5-113">Example 2: Add a rule to a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$ruleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"

$rule2 = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
$ruleCollection.AddRule($rule2)
```

<span data-ttu-id="4fce5-114">Ebben a példában egy új szabálygyűjteményt hoz létre egy szabály alapján, majd hozzáad egy második szabályt a szabálygyűjteményhez az AddRule metódussal a szabálygyűjtemény-objektumon.</span><span class="sxs-lookup"><span data-stu-id="4fce5-114">This example creates a new network rule collection with one rule and then adds a second rule to the rule collection using method AddRule on the rule collection object.</span></span> <span data-ttu-id="4fce5-115">Az adott szabálygyűjteményben minden szabálynévnek egyedi névvel kell lennie, és a kis- és a nagy- és a kis</span><span class="sxs-lookup"><span data-stu-id="4fce5-115">Each rule name in a given rule collection must have a unique name and is case insensitive.</span></span>

### <span data-ttu-id="4fce5-116">3. példa: Szabály begyűjtése szabálygyűjteményből</span><span class="sxs-lookup"><span data-stu-id="4fce5-116">Example 3: Get a rule from a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$ruleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"
$getRule=$ruleCollection.GetRuleByName("ALL-UDP-traffic")
```

<span data-ttu-id="4fce5-117">Ebben a példában egy új hálózatszabály-gyűjteményt hoz létre egy s szabály alapján, majd név szerint, a GetRuleByName hívási metódust kapja meg a szabálygyűjtemény-objektumon.</span><span class="sxs-lookup"><span data-stu-id="4fce5-117">This example creates a new network rule collection with one rule and then gets the rule by name, calling method GetRuleByName on the rule collection object.</span></span> <span data-ttu-id="4fce5-118">A GetRuleByName metódus szabályneve a kis- és</span><span class="sxs-lookup"><span data-stu-id="4fce5-118">The rule name for method GetRuleByName is case-insensitive.</span></span>

### <span data-ttu-id="4fce5-119">4. példa: Szabály eltávolítása szabálygyűjteményből</span><span class="sxs-lookup"><span data-stu-id="4fce5-119">Example 4: Remove a rule from a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$rule2 = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
$ruleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1, $rule2 -ActionType "Allow"
$ruleCollection.RemoveRuleByName("ALL-udp-traffic")
```

<span data-ttu-id="4fce5-120">Ebben a példában egy új hálózatszabály-gyűjteményt hoz létre két sszabályokkal, majd eltávolítja az első szabályt a szabálygyűjteményből a RemoveRuleByName hívási módszerrel a szabálygyűjtemény-objektumon.</span><span class="sxs-lookup"><span data-stu-id="4fce5-120">This example creates a new network rule collection with two rules and then removes the first rule from the rule collection by calling method RemoveRuleByName on the rule collection object.</span></span> <span data-ttu-id="4fce5-121">A RemoveRuleByName metódus szabályneve a kis- és</span><span class="sxs-lookup"><span data-stu-id="4fce5-121">The rule name for method RemoveRuleByName is case-insensitive.</span></span>

## <span data-ttu-id="4fce5-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4fce5-122">PARAMETERS</span></span>

### <span data-ttu-id="4fce5-123">-ActionType</span><span class="sxs-lookup"><span data-stu-id="4fce5-123">-ActionType</span></span>
<span data-ttu-id="4fce5-124">Meghatározza a szabály forgalomegyeztetési feltételeihez szükséges műveletet.</span><span class="sxs-lookup"><span data-stu-id="4fce5-124">Specifies the action to be taken for traffic matching conditions of this rule.</span></span> <span data-ttu-id="4fce5-125">Az elfogadott műveletek "Megengedve" vagy "Elutasítás".</span><span class="sxs-lookup"><span data-stu-id="4fce5-125">Accepted actions are "Allow" or "Deny".</span></span>

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

### <span data-ttu-id="4fce5-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fce5-126">-DefaultProfile</span></span>
<span data-ttu-id="4fce5-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4fce5-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4fce5-128">-Name</span><span class="sxs-lookup"><span data-stu-id="4fce5-128">-Name</span></span>
<span data-ttu-id="4fce5-129">A hálózati szabálycsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4fce5-129">Specifies the name of this network rule collection.</span></span> <span data-ttu-id="4fce5-130">A névnek minden hálózati szabálycsoportban egyedinek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="4fce5-130">The name must be unique across all network rule collection.</span></span>

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

### <span data-ttu-id="4fce5-131">-Priority</span><span class="sxs-lookup"><span data-stu-id="4fce5-131">-Priority</span></span>
<span data-ttu-id="4fce5-132">A szabálygyűjtemény prioritását határozza meg.</span><span class="sxs-lookup"><span data-stu-id="4fce5-132">Specifies the priority of this rule collection.</span></span> <span data-ttu-id="4fce5-133">A prioritás 100 és 65000 közötti szám.</span><span class="sxs-lookup"><span data-stu-id="4fce5-133">Priority is a number between 100 and 65000.</span></span> <span data-ttu-id="4fce5-134">Minél kisebb a szám, annál nagyobb a prioritás.</span><span class="sxs-lookup"><span data-stu-id="4fce5-134">The smaller the number, the higher the priority.</span></span>

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

### <span data-ttu-id="4fce5-135">-Rule</span><span class="sxs-lookup"><span data-stu-id="4fce5-135">-Rule</span></span>
<span data-ttu-id="4fce5-136">Az ebben a gyűjteményben csoportosított szabályok listáját határozza meg.</span><span class="sxs-lookup"><span data-stu-id="4fce5-136">Specifies the list of rules to be grouped under this collection.</span></span>

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

### <span data-ttu-id="4fce5-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4fce5-137">-Confirm</span></span>
<span data-ttu-id="4fce5-138">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="4fce5-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fce5-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fce5-139">-WhatIf</span></span>
<span data-ttu-id="4fce5-140">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="4fce5-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4fce5-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4fce5-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4fce5-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fce5-142">CommonParameters</span></span>
<span data-ttu-id="4fce5-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fce5-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fce5-144">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fce5-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fce5-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4fce5-145">INPUTS</span></span>

### <span data-ttu-id="4fce5-146">Nincs</span><span class="sxs-lookup"><span data-stu-id="4fce5-146">None</span></span>

## <span data-ttu-id="4fce5-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4fce5-147">OUTPUTS</span></span>

### <span data-ttu-id="4fce5-148">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="4fce5-148">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection</span></span>

## <span data-ttu-id="4fce5-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4fce5-149">NOTES</span></span>

## <span data-ttu-id="4fce5-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4fce5-150">RELATED LINKS</span></span>

[<span data-ttu-id="4fce5-151">New-AzFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="4fce5-151">New-AzFirewallNetworkRule</span></span>](./New-AzFirewallNetworkRule.md)

[<span data-ttu-id="4fce5-152">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="4fce5-152">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="4fce5-153">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="4fce5-153">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
