---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallnatrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRuleCollection.md
ms.openlocfilehash: 4ba57fd922319eb2be6ba001c723b3e668bce59e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194030"
---
# <span data-ttu-id="d7e6d-101">New-AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="d7e6d-101">New-AzFirewallNatRuleCollection</span></span>

## <span data-ttu-id="d7e6d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d7e6d-102">SYNOPSIS</span></span>
<span data-ttu-id="d7e6d-103">Tűzfal-CÍMFORDÍTÁSi szabályok gyűjteményét hozza létre.</span><span class="sxs-lookup"><span data-stu-id="d7e6d-103">Creates a collection of Firewall NAT rules.</span></span>

## <span data-ttu-id="d7e6d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d7e6d-104">SYNTAX</span></span>

```
New-AzFirewallNatRuleCollection -Name <String> -Priority <UInt32> -Rule <PSAzureFirewallNatRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7e6d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d7e6d-105">DESCRIPTION</span></span>
<span data-ttu-id="d7e6d-106">A **New-AzFirewallNatRuleCollection** parancsmag a tűzfal NAT-szabályainak gyűjteményét hozza létre.</span><span class="sxs-lookup"><span data-stu-id="d7e6d-106">The **New-AzFirewallNatRuleCollection** cmdlet creates a collection of Firewall NAT Rules.</span></span>

## <span data-ttu-id="d7e6d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d7e6d-107">EXAMPLES</span></span>

### <span data-ttu-id="d7e6d-108">Példa 1: gyűjtemény létrehozása egyetlen szabállyal</span><span class="sxs-lookup"><span data-stu-id="d7e6d-108">Example 1: Create a collection with one rule</span></span>
```powershell
$rule1 = New-AzFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "80" -TranslatedAddress "10.0.0.2" -TranslatedPort "8080"
New-AzFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 1000 -Rule $rule1
```

<span data-ttu-id="d7e6d-109">Ebben a példában egy-egy szabályt tartalmazó gyűjtemény jön létre.</span><span class="sxs-lookup"><span data-stu-id="d7e6d-109">This example creates a collection with one rule.</span></span> <span data-ttu-id="d7e6d-110">Minden olyan forgalom, amely megfelel az 1. $rule megadott feltételeknek, a lefordított címre és DNAT'ed fog szerepelni.</span><span class="sxs-lookup"><span data-stu-id="d7e6d-110">All traffic that matches the conditions identified in $rule1 will be DNAT'ed to translated address and port.</span></span>

### <span data-ttu-id="d7e6d-111">2. példa: szabály hozzáadása egy szabály-gyűjteményhez</span><span class="sxs-lookup"><span data-stu-id="d7e6d-111">Example 2: Add a rule to a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallNatRule -Name R1 -Protocol "UDP","TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "80" -TranslatedAddress "10.0.0.2" -TranslatedPort "8080"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 100 -Rule $rule1

$rule2 = New-AzFirewallNatRule -Name R2 -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "443" -TranslatedAddress "10.0.0.2" -TranslatedPort "8443"
$ruleCollection.AddRule($rule2)
```

<span data-ttu-id="d7e6d-112">Ebben a példában egy új NAT-szabályt hoz létre egy szabállyal, majd egy második szabályt ad hozzá a szabályok gyűjteményéhez a szabály-gyűjtemény AddRule.</span><span class="sxs-lookup"><span data-stu-id="d7e6d-112">This example creates a new NAT rule collection with one rule and then adds a second rule to the rule collection using method AddRule on the rule collection object.</span></span> <span data-ttu-id="d7e6d-113">Egy adott szabálygyűjtemény mindegyik szabályának egyedi névvel kell rendelkeznie, és a kis-és nagybetűk megkülönböztetésére is szükség van.</span><span class="sxs-lookup"><span data-stu-id="d7e6d-113">Each rule name in a given rule collection must have an unique name and is case insensitive.</span></span>

### <span data-ttu-id="d7e6d-114">3. példa: szabály beszerzése egy szabály-gyűjteményből</span><span class="sxs-lookup"><span data-stu-id="d7e6d-114">Example 3: Get a rule from a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallNatRule -Name R1 -Protocol "TCP" -SourceAddress "10.0.0.0/24" -DestinationAddress "10.0.1.0/24" -DestinationPort "443" -TranslatedAddress "10.0.0.2" -TranslatedPort "8443"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 100 -Rule $rule1

$rule=$ruleCollection.GetRuleByName("r1")
```

<span data-ttu-id="d7e6d-115">Ebben a példában egy új NAT-szabályt hoz létre egy szabállyal, majd a szabályt név szerint, a hívási módszer GetRuleByName a szabály-gyűjtemény objektumban kapja.</span><span class="sxs-lookup"><span data-stu-id="d7e6d-115">This example creates a new NAT rule collection with one rule and then gets the rule by name, calling method GetRuleByName on the rule collection object.</span></span> <span data-ttu-id="d7e6d-116">A GetRuleByName metódus szabályának neve megkülönbözteti a kis-és nagybetűket.</span><span class="sxs-lookup"><span data-stu-id="d7e6d-116">The rule name for method GetRuleByName is case-insensitive.</span></span>

### <span data-ttu-id="d7e6d-117">4. példa: szabály eltávolítása egy szabály-gyűjteményből</span><span class="sxs-lookup"><span data-stu-id="d7e6d-117">Example 4: Remove a rule from a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallNatRule -Name R1 -Protocol "UDP","TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "80" -TranslatedAddress "10.0.0.2" -TranslatedPort "8080"
$rule2 = New-AzFirewallNatRule -Name R2 -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "443" -TranslatedAddress "10.0.0.2" -TranslatedPort "8443"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 100 -Rule $rule1, $rule2
$ruleCollection.RemoveRuleByName("r1")
```

<span data-ttu-id="d7e6d-118">Ebben a példában egy új NAT-szabályt hoz létre két szabállyal, majd eltávolítja az első szabályt a szabály gyűjteményből a RemoveRuleByName metódussal.</span><span class="sxs-lookup"><span data-stu-id="d7e6d-118">This example creates a new NAT rule collection with two rules and then removes the first rule from the rule collection by calling method RemoveRuleByName on the rule collection object.</span></span> <span data-ttu-id="d7e6d-119">A RemoveRuleByName metódus szabályának neve megkülönbözteti a kis-és nagybetűket.</span><span class="sxs-lookup"><span data-stu-id="d7e6d-119">The rule name for method RemoveRuleByName is case-insensitive.</span></span>

## <span data-ttu-id="d7e6d-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d7e6d-120">PARAMETERS</span></span>

### <span data-ttu-id="d7e6d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7e6d-121">-DefaultProfile</span></span>
<span data-ttu-id="d7e6d-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d7e6d-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7e6d-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d7e6d-123">-Name</span></span>
<span data-ttu-id="d7e6d-124">A NAT-szabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7e6d-124">Specifies the name of this NAT rule.</span></span> <span data-ttu-id="d7e6d-125">A névnek egyedinek kell lennie egy szabály-gyűjteményen belül.</span><span class="sxs-lookup"><span data-stu-id="d7e6d-125">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="d7e6d-126">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="d7e6d-126">-Priority</span></span>
<span data-ttu-id="d7e6d-127">A szabály prioritását adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7e6d-127">Specifies the priority of this rule.</span></span> <span data-ttu-id="d7e6d-128">A prioritás az 100 és az 65000 közötti szám.</span><span class="sxs-lookup"><span data-stu-id="d7e6d-128">Priority is a number between 100 and 65000.</span></span> <span data-ttu-id="d7e6d-129">Minél kisebb a szám, annál nagyobb a prioritás.</span><span class="sxs-lookup"><span data-stu-id="d7e6d-129">The smaller the number, the bigger the priority.</span></span>

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

### <span data-ttu-id="d7e6d-130">-Szabály</span><span class="sxs-lookup"><span data-stu-id="d7e6d-130">-Rule</span></span>
<span data-ttu-id="d7e6d-131">Az ebben a gyűjteményben csoportosítani kívánt szabályok listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7e6d-131">Specifies the list of rules to be grouped under this collection.</span></span>

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

### <span data-ttu-id="d7e6d-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d7e6d-132">-Confirm</span></span>
<span data-ttu-id="d7e6d-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d7e6d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7e6d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7e6d-134">-WhatIf</span></span>
<span data-ttu-id="d7e6d-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d7e6d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7e6d-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d7e6d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7e6d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7e6d-137">CommonParameters</span></span>
<span data-ttu-id="d7e6d-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d7e6d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7e6d-139">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7e6d-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7e6d-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7e6d-140">INPUTS</span></span>

### <span data-ttu-id="d7e6d-141">Nincs</span><span class="sxs-lookup"><span data-stu-id="d7e6d-141">None</span></span>

## <span data-ttu-id="d7e6d-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7e6d-142">OUTPUTS</span></span>

### <span data-ttu-id="d7e6d-143">Microsoft. Azure. commands. Network. models. PSAzureFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="d7e6d-143">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection</span></span>

## <span data-ttu-id="d7e6d-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d7e6d-144">NOTES</span></span>

## <span data-ttu-id="d7e6d-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d7e6d-145">RELATED LINKS</span></span>

[<span data-ttu-id="d7e6d-146">Új – AzFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="d7e6d-146">New-AzFirewallNatRule</span></span>](./New-AzFirewallNatRule.md)

[<span data-ttu-id="d7e6d-147">Új – AzFirewall</span><span class="sxs-lookup"><span data-stu-id="d7e6d-147">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="d7e6d-148">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="d7e6d-148">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
