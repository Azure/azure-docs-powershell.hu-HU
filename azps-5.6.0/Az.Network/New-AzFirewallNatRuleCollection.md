---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallnatrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRuleCollection.md
ms.openlocfilehash: d637767f21a34daf5afaf1f2a44e9ebc9b80934a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941066"
---
# <span data-ttu-id="96796-101">New-AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="96796-101">New-AzFirewallNatRuleCollection</span></span>

## <span data-ttu-id="96796-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96796-102">SYNOPSIS</span></span>
<span data-ttu-id="96796-103">Tűzfal NAT-szabályok gyűjteményét hozza létre.</span><span class="sxs-lookup"><span data-stu-id="96796-103">Creates a collection of Firewall NAT rules.</span></span>

## <span data-ttu-id="96796-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="96796-104">SYNTAX</span></span>

```
New-AzFirewallNatRuleCollection -Name <String> -Priority <UInt32> -Rule <PSAzureFirewallNatRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96796-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="96796-105">DESCRIPTION</span></span>
<span data-ttu-id="96796-106">A **New-AzFirewallNatRuleCollection** parancsmag tűzfal NAT-szabályok gyűjteményét hozza létre.</span><span class="sxs-lookup"><span data-stu-id="96796-106">The **New-AzFirewallNatRuleCollection** cmdlet creates a collection of Firewall NAT Rules.</span></span>

## <span data-ttu-id="96796-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="96796-107">EXAMPLES</span></span>

### <span data-ttu-id="96796-108">1. példa: Gyűjtemény létrehozása egyetlen s szabálysal</span><span class="sxs-lookup"><span data-stu-id="96796-108">Example 1: Create a collection with one rule</span></span>
```powershell
$rule1 = New-AzFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "80" -TranslatedAddress "10.0.0.2" -TranslatedPort "8080"
New-AzFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 1000 -Rule $rule1
```

<span data-ttu-id="96796-109">Ez a példa létrehoz egy gyűjteményt egyetlen s szabálysal.</span><span class="sxs-lookup"><span data-stu-id="96796-109">This example creates a collection with one rule.</span></span> <span data-ttu-id="96796-110">Az $rule 1-ben meghatározott feltételeknek megfelelő forgalmat a SZÖVEG.ISM'et lefordított címre és portra fordítjuk.</span><span class="sxs-lookup"><span data-stu-id="96796-110">All traffic that matches the conditions identified in $rule1 will be DNAT'ed to translated address and port.</span></span>

### <span data-ttu-id="96796-111">2. példa: Szabály hozzáadása szabálygyűjteményhez</span><span class="sxs-lookup"><span data-stu-id="96796-111">Example 2: Add a rule to a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallNatRule -Name R1 -Protocol "UDP","TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "80" -TranslatedAddress "10.0.0.2" -TranslatedPort "8080"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 100 -Rule $rule1

$rule2 = New-AzFirewallNatRule -Name R2 -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "443" -TranslatedAddress "10.0.0.2" -TranslatedPort "8443"
$ruleCollection.AddRule($rule2)
```

<span data-ttu-id="96796-112">Ebben a példában egy új NAT-szabálygyűjteményt hoz létre egy s szabály alapján, majd hozzáad egy második szabályt a szabálygyűjteményhez az AddRule metódussal a szabálygyűjtemény-objektumon.</span><span class="sxs-lookup"><span data-stu-id="96796-112">This example creates a new NAT rule collection with one rule and then adds a second rule to the rule collection using method AddRule on the rule collection object.</span></span> <span data-ttu-id="96796-113">Az adott szabálygyűjteményben minden szabálynévnek egyedi névvel kell lennie, és a kis- és a nagy- és a kis- és a nagy- és a kis-</span><span class="sxs-lookup"><span data-stu-id="96796-113">Each rule name in a given rule collection must have an unique name and is case insensitive.</span></span>

### <span data-ttu-id="96796-114">3. példa: Szabály begyűjtése szabálygyűjteményből</span><span class="sxs-lookup"><span data-stu-id="96796-114">Example 3: Get a rule from a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallNatRule -Name R1 -Protocol "TCP" -SourceAddress "10.0.0.0/24" -DestinationAddress "10.0.1.0/24" -DestinationPort "443" -TranslatedAddress "10.0.0.2" -TranslatedPort "8443"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 100 -Rule $rule1

$rule=$ruleCollection.GetRuleByName("r1")
```

<span data-ttu-id="96796-115">Ebben a példában egy új NAT-szabálygyűjteményt hoz létre egy s szabály alapján, majd név szerint, a GetRuleByName hívási metódust kapja meg a szabálygyűjtemény-objektumon.</span><span class="sxs-lookup"><span data-stu-id="96796-115">This example creates a new NAT rule collection with one rule and then gets the rule by name, calling method GetRuleByName on the rule collection object.</span></span> <span data-ttu-id="96796-116">A GetRuleByName metódus szabályneve a kis- és</span><span class="sxs-lookup"><span data-stu-id="96796-116">The rule name for method GetRuleByName is case-insensitive.</span></span>

### <span data-ttu-id="96796-117">4. példa: Szabály eltávolítása szabálygyűjteményből</span><span class="sxs-lookup"><span data-stu-id="96796-117">Example 4: Remove a rule from a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallNatRule -Name R1 -Protocol "UDP","TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "80" -TranslatedAddress "10.0.0.2" -TranslatedPort "8080"
$rule2 = New-AzFirewallNatRule -Name R2 -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "443" -TranslatedAddress "10.0.0.2" -TranslatedPort "8443"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 100 -Rule $rule1, $rule2
$ruleCollection.RemoveRuleByName("r1")
```

<span data-ttu-id="96796-118">Ez a példa létrehoz egy új NAT-szabálygyűjteményt két sszabályokkal, majd eltávolítja az első szabályt a szabálygyűjteményből a RemoveRuleByName hívási módszerrel a szabálygyűjtemény-objektumon.</span><span class="sxs-lookup"><span data-stu-id="96796-118">This example creates a new NAT rule collection with two rules and then removes the first rule from the rule collection by calling method RemoveRuleByName on the rule collection object.</span></span> <span data-ttu-id="96796-119">A RemoveRuleByName metódus szabályneve a kis- és</span><span class="sxs-lookup"><span data-stu-id="96796-119">The rule name for method RemoveRuleByName is case-insensitive.</span></span>

## <span data-ttu-id="96796-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="96796-120">PARAMETERS</span></span>

### <span data-ttu-id="96796-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96796-121">-DefaultProfile</span></span>
<span data-ttu-id="96796-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="96796-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96796-123">-Name</span><span class="sxs-lookup"><span data-stu-id="96796-123">-Name</span></span>
<span data-ttu-id="96796-124">A NAT-szabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="96796-124">Specifies the name of this NAT rule.</span></span> <span data-ttu-id="96796-125">A névnek egyedinek kell lennie egy szabálygyűjteményben.</span><span class="sxs-lookup"><span data-stu-id="96796-125">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="96796-126">-Priority</span><span class="sxs-lookup"><span data-stu-id="96796-126">-Priority</span></span>
<span data-ttu-id="96796-127">Megadja a szabály prioritását.</span><span class="sxs-lookup"><span data-stu-id="96796-127">Specifies the priority of this rule.</span></span> <span data-ttu-id="96796-128">A prioritás 100 és 65000 közötti szám.</span><span class="sxs-lookup"><span data-stu-id="96796-128">Priority is a number between 100 and 65000.</span></span> <span data-ttu-id="96796-129">Minél kisebb a szám, annál nagyobb a prioritás.</span><span class="sxs-lookup"><span data-stu-id="96796-129">The smaller the number, the bigger the priority.</span></span>

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

### <span data-ttu-id="96796-130">-Rule</span><span class="sxs-lookup"><span data-stu-id="96796-130">-Rule</span></span>
<span data-ttu-id="96796-131">Az ebben a gyűjteményben csoportosított szabályok listáját határozza meg.</span><span class="sxs-lookup"><span data-stu-id="96796-131">Specifies the list of rules to be grouped under this collection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96796-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="96796-132">-Confirm</span></span>
<span data-ttu-id="96796-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="96796-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96796-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96796-134">-WhatIf</span></span>
<span data-ttu-id="96796-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="96796-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96796-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="96796-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96796-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96796-137">CommonParameters</span></span>
<span data-ttu-id="96796-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96796-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96796-139">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96796-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96796-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="96796-140">INPUTS</span></span>

### <span data-ttu-id="96796-141">Nincs</span><span class="sxs-lookup"><span data-stu-id="96796-141">None</span></span>

## <span data-ttu-id="96796-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="96796-142">OUTPUTS</span></span>

### <span data-ttu-id="96796-143">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="96796-143">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection</span></span>

## <span data-ttu-id="96796-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="96796-144">NOTES</span></span>

## <span data-ttu-id="96796-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="96796-145">RELATED LINKS</span></span>

[<span data-ttu-id="96796-146">New-AzFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="96796-146">New-AzFirewallNatRule</span></span>](./New-AzFirewallNatRule.md)

[<span data-ttu-id="96796-147">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="96796-147">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="96796-148">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="96796-148">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
