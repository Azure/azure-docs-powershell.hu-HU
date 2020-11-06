---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermfirewallnatrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallNatRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallNatRuleCollection.md
ms.openlocfilehash: 12b45dd5fd62dabb2650f121f52a539962315513
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494045"
---
# <span data-ttu-id="08731-101">New-AzureRmFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="08731-101">New-AzureRmFirewallNatRuleCollection</span></span>

## <span data-ttu-id="08731-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="08731-102">SYNOPSIS</span></span>
<span data-ttu-id="08731-103">Tűzfal-CÍMFORDÍTÁSi szabályok gyűjteményét hozza létre.</span><span class="sxs-lookup"><span data-stu-id="08731-103">Creates a collection of Firewall NAT rules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="08731-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="08731-104">SYNTAX</span></span>

```
New-AzureRmFirewallNatRuleCollection -Name <String> -Priority <UInt32>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08731-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="08731-105">DESCRIPTION</span></span>
<span data-ttu-id="08731-106">A **New-AzureRmFirewallNatRuleCollection** parancsmag a tűzfal NAT-szabályainak gyűjteményét hozza létre.</span><span class="sxs-lookup"><span data-stu-id="08731-106">The **New-AzureRmFirewallNatRuleCollection** cmdlet creates a collection of Firewall NAT Rules.</span></span>

## <span data-ttu-id="08731-107">Példák</span><span class="sxs-lookup"><span data-stu-id="08731-107">EXAMPLES</span></span>

### <span data-ttu-id="08731-108">1: gyűjtemény létrehozása egyetlen szabállyal</span><span class="sxs-lookup"><span data-stu-id="08731-108">1:  Create a collection with one rule</span></span>
```
$rule1 = New-AzureRmFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "80" -TranslatedAddress "10.0.0.2" -TranslatedPort "8080"
New-AzureRmFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 1000 -Rule $rule1
```

<span data-ttu-id="08731-109">Ebben a példában egy-egy szabályt tartalmazó gyűjtemény jön létre.</span><span class="sxs-lookup"><span data-stu-id="08731-109">This example creates a collection with one rule.</span></span> <span data-ttu-id="08731-110">Minden olyan forgalom, amely megfelel az 1. $rule megadott feltételeknek, a lefordított címre és DNAT'ed fog szerepelni.</span><span class="sxs-lookup"><span data-stu-id="08731-110">All traffic that matches the conditions identified in $rule1 will be DNAT'ed to translated address and port.</span></span>

### <span data-ttu-id="08731-111">2: szabály hozzáadása egy szabály-gyűjteményhez</span><span class="sxs-lookup"><span data-stu-id="08731-111">2:  Add a rule to a rule collection</span></span>
```
$rule1 = New-AzureRmFirewallNatRule -Name R1 -Protocol "UDP","TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "80" -TranslatedAddress "10.0.0.2" -TranslatedPort "8080"
$ruleCollection = New-AzureRmFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 100 -Rule $rule1

$rule2 = New-AzureRmFirewallNatRule -Name R2 -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "443" -TranslatedAddress "10.0.0.2" -TranslatedPort "8443"
$ruleCollection.AddRule($rule2)
```

<span data-ttu-id="08731-112">Ebben a példában egy új NAT-szabályt hoz létre egy szabállyal, majd egy második szabályt ad hozzá a szabályok gyűjteményéhez a szabály-gyűjtemény AddRule.</span><span class="sxs-lookup"><span data-stu-id="08731-112">This example creates a new NAT rule collection with one rule and then adds a second rule to the rule collection using method AddRule on the rule collection object.</span></span> <span data-ttu-id="08731-113">Egy adott szabálygyűjtemény mindegyik szabályának egyedi névvel kell rendelkeznie, és a kis-és nagybetűk megkülönböztetésére is szükség van.</span><span class="sxs-lookup"><span data-stu-id="08731-113">Each rule name in a given rule collection must have an unique name and is case insensitive.</span></span>

### <span data-ttu-id="08731-114">3: szabály kérése egy szabály-gyűjteményből</span><span class="sxs-lookup"><span data-stu-id="08731-114">3:  Get a rule from a rule collection</span></span>
```
$rule1 = New-AzureRmFirewallNatRule -Name R1 -Protocol "TCP" -SourceAddress "10.0.0.0/24" -DestinationAddress "10.0.1.0/24" -DestinationPort "443" -TranslatedAddress "10.0.0.2" -TranslatedPort "8443"
$ruleCollection = New-AzureRmFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 100 -Rule $rule1

$rule=$ruleCollection.GetRuleByName("r1")
```

<span data-ttu-id="08731-115">Ebben a példában egy új NAT-szabályt hoz létre egy szabállyal, majd a szabályt név szerint, a hívási módszer GetRuleByName a szabály-gyűjtemény objektumban kapja.</span><span class="sxs-lookup"><span data-stu-id="08731-115">This example creates a new NAT rule collection with one rule and then gets the rule by name, calling method GetRuleByName on the rule collection object.</span></span> <span data-ttu-id="08731-116">A GetRuleByName metódus szabályának neve megkülönbözteti a kis-és nagybetűket.</span><span class="sxs-lookup"><span data-stu-id="08731-116">The rule name for method GetRuleByName is case-insensitive.</span></span>

### <span data-ttu-id="08731-117">4: szabály eltávolítása a szabályok gyűjteményéből</span><span class="sxs-lookup"><span data-stu-id="08731-117">4:  Remove a rule from a rule collection</span></span>
```
$rule1 = New-AzureRmFirewallNatRule -Name R1 -Protocol "UDP","TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "80" -TranslatedAddress "10.0.0.2" -TranslatedPort "8080"
$rule2 = New-AzureRmFirewallNatRule -Name R2 -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "443" -TranslatedAddress "10.0.0.2" -TranslatedPort "8443"
$ruleCollection = New-AzureRmFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 100 -Rule $rule1, $rule2
$ruleCollection.RemoveRuleByName("r1")
```

<span data-ttu-id="08731-118">Ebben a példában egy új NAT-szabályt hoz létre két szabállyal, majd eltávolítja az első szabályt a szabály gyűjteményből a RemoveRuleByName metódussal.</span><span class="sxs-lookup"><span data-stu-id="08731-118">This example creates a new NAT rule collection with two rules and then removes the first rule from the rule collection by calling method RemoveRuleByName on the rule collection object.</span></span> <span data-ttu-id="08731-119">A RemoveRuleByName metódus szabályának neve megkülönbözteti a kis-és nagybetűket.</span><span class="sxs-lookup"><span data-stu-id="08731-119">The rule name for method RemoveRuleByName is case-insensitive.</span></span>

## <span data-ttu-id="08731-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="08731-120">PARAMETERS</span></span>

### <span data-ttu-id="08731-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08731-121">-DefaultProfile</span></span>
<span data-ttu-id="08731-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="08731-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08731-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="08731-123">-Name</span></span>
<span data-ttu-id="08731-124">A NAT-szabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="08731-124">Specifies the name of this NAT rule.</span></span> <span data-ttu-id="08731-125">A névnek egyedinek kell lennie egy szabály-gyűjteményen belül.</span><span class="sxs-lookup"><span data-stu-id="08731-125">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="08731-126">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="08731-126">-Priority</span></span>
<span data-ttu-id="08731-127">A szabály prioritását adja meg.</span><span class="sxs-lookup"><span data-stu-id="08731-127">Specifies the priority of this rule.</span></span> <span data-ttu-id="08731-128">A prioritás az 100 és az 65000 közötti szám.</span><span class="sxs-lookup"><span data-stu-id="08731-128">Priority is a number between 100 and 65000.</span></span> <span data-ttu-id="08731-129">Minél kisebb a szám, annál nagyobb a prioritás.</span><span class="sxs-lookup"><span data-stu-id="08731-129">The smaller the number, the bigger the priority.</span></span>

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

### <span data-ttu-id="08731-130">-Szabály</span><span class="sxs-lookup"><span data-stu-id="08731-130">-Rule</span></span>
<span data-ttu-id="08731-131">Az ebben a gyűjteményben csoportosítani kívánt szabályok listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="08731-131">Specifies the list of rules to be grouped under this collection.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08731-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="08731-132">-Confirm</span></span>
<span data-ttu-id="08731-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="08731-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08731-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08731-134">-WhatIf</span></span>
<span data-ttu-id="08731-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="08731-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08731-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="08731-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08731-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08731-137">CommonParameters</span></span>
<span data-ttu-id="08731-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="08731-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08731-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08731-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08731-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="08731-140">INPUTS</span></span>

### <span data-ttu-id="08731-141">Nincs</span><span class="sxs-lookup"><span data-stu-id="08731-141">None</span></span>
<span data-ttu-id="08731-142">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="08731-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="08731-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="08731-143">OUTPUTS</span></span>

### <span data-ttu-id="08731-144">Microsoft. Azure. commands. Network. models. PSFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="08731-144">Microsoft.Azure.Commands.Network.Models.PSFirewallNatRuleCollection</span></span>

## <span data-ttu-id="08731-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="08731-145">NOTES</span></span>

## <span data-ttu-id="08731-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="08731-146">RELATED LINKS</span></span>

[<span data-ttu-id="08731-147">Új – AzureRmFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="08731-147">New-AzureRmFirewallNatRule</span></span>](./New-AzureRmFirewallNatRule.md)

[<span data-ttu-id="08731-148">Új – AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="08731-148">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)

[<span data-ttu-id="08731-149">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="08731-149">Get-AzureRmFirewall</span></span>](./Get-AzureRmFirewall.md)
