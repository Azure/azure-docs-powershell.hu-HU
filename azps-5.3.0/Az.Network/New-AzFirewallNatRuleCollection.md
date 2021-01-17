---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallnatrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRuleCollection.md
ms.openlocfilehash: 4ba57fd922319eb2be6ba001c723b3e668bce59e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469033"
---
# <span data-ttu-id="6cbce-101">New-AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="6cbce-101">New-AzFirewallNatRuleCollection</span></span>

## <span data-ttu-id="6cbce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6cbce-102">SYNOPSIS</span></span>
<span data-ttu-id="6cbce-103">Tűzfal NAT-szabályok gyűjteményét hozza létre.</span><span class="sxs-lookup"><span data-stu-id="6cbce-103">Creates a collection of Firewall NAT rules.</span></span>

## <span data-ttu-id="6cbce-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6cbce-104">SYNTAX</span></span>

```
New-AzFirewallNatRuleCollection -Name <String> -Priority <UInt32> -Rule <PSAzureFirewallNatRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6cbce-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6cbce-105">DESCRIPTION</span></span>
<span data-ttu-id="6cbce-106">A **New-AzFirewallNatRuleCollection** parancsmag tűzfal NAT-szabályok gyűjteményét hozza létre.</span><span class="sxs-lookup"><span data-stu-id="6cbce-106">The **New-AzFirewallNatRuleCollection** cmdlet creates a collection of Firewall NAT Rules.</span></span>

## <span data-ttu-id="6cbce-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6cbce-107">EXAMPLES</span></span>

### <span data-ttu-id="6cbce-108">1. példa: Gyűjtemény létrehozása egyetlen s szabálysal</span><span class="sxs-lookup"><span data-stu-id="6cbce-108">Example 1: Create a collection with one rule</span></span>
```powershell
$rule1 = New-AzFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "80" -TranslatedAddress "10.0.0.2" -TranslatedPort "8080"
New-AzFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 1000 -Rule $rule1
```

<span data-ttu-id="6cbce-109">Ez a példa létrehoz egy gyűjteményt egyetlen s szabálysal.</span><span class="sxs-lookup"><span data-stu-id="6cbce-109">This example creates a collection with one rule.</span></span> <span data-ttu-id="6cbce-110">Az $rule 1-ben meghatározott feltételeknek megfelelő forgalmat a SZÖVEG.ISM'et lefordított címre és portra fordítjuk.</span><span class="sxs-lookup"><span data-stu-id="6cbce-110">All traffic that matches the conditions identified in $rule1 will be DNAT'ed to translated address and port.</span></span>

### <span data-ttu-id="6cbce-111">2. példa: Szabály hozzáadása szabálygyűjteményhez</span><span class="sxs-lookup"><span data-stu-id="6cbce-111">Example 2: Add a rule to a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallNatRule -Name R1 -Protocol "UDP","TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "80" -TranslatedAddress "10.0.0.2" -TranslatedPort "8080"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 100 -Rule $rule1

$rule2 = New-AzFirewallNatRule -Name R2 -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "443" -TranslatedAddress "10.0.0.2" -TranslatedPort "8443"
$ruleCollection.AddRule($rule2)
```

<span data-ttu-id="6cbce-112">Ebben a példában egy új NAT-szabálygyűjteményt hoz létre egy s szabály alapján, majd hozzáad egy második szabályt a szabálygyűjteményhez az AddRule metódussal a szabálygyűjtemény-objektumon.</span><span class="sxs-lookup"><span data-stu-id="6cbce-112">This example creates a new NAT rule collection with one rule and then adds a second rule to the rule collection using method AddRule on the rule collection object.</span></span> <span data-ttu-id="6cbce-113">Az adott szabálygyűjteményben minden szabálynévnek egyedi névvel kell lennie, és a kis- és a nagy- és a kis</span><span class="sxs-lookup"><span data-stu-id="6cbce-113">Each rule name in a given rule collection must have an unique name and is case insensitive.</span></span>

### <span data-ttu-id="6cbce-114">3. példa: Szabály begyűjtése szabálygyűjteményből</span><span class="sxs-lookup"><span data-stu-id="6cbce-114">Example 3: Get a rule from a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallNatRule -Name R1 -Protocol "TCP" -SourceAddress "10.0.0.0/24" -DestinationAddress "10.0.1.0/24" -DestinationPort "443" -TranslatedAddress "10.0.0.2" -TranslatedPort "8443"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 100 -Rule $rule1

$rule=$ruleCollection.GetRuleByName("r1")
```

<span data-ttu-id="6cbce-115">Ebben a példában egy új NAT-szabálygyűjteményt hoz létre egy s szabály alapján, majd név szerint, a GetRuleByName hívási metódust kapja meg a szabálygyűjtemény-objektumon.</span><span class="sxs-lookup"><span data-stu-id="6cbce-115">This example creates a new NAT rule collection with one rule and then gets the rule by name, calling method GetRuleByName on the rule collection object.</span></span> <span data-ttu-id="6cbce-116">A GetRuleByName metódus szabályneve a kis- és</span><span class="sxs-lookup"><span data-stu-id="6cbce-116">The rule name for method GetRuleByName is case-insensitive.</span></span>

### <span data-ttu-id="6cbce-117">4. példa: Szabály eltávolítása szabálygyűjteményből</span><span class="sxs-lookup"><span data-stu-id="6cbce-117">Example 4: Remove a rule from a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallNatRule -Name R1 -Protocol "UDP","TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "80" -TranslatedAddress "10.0.0.2" -TranslatedPort "8080"
$rule2 = New-AzFirewallNatRule -Name R2 -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "443" -TranslatedAddress "10.0.0.2" -TranslatedPort "8443"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 100 -Rule $rule1, $rule2
$ruleCollection.RemoveRuleByName("r1")
```

<span data-ttu-id="6cbce-118">Ez a példa létrehoz egy új NAT-szabálygyűjteményt két sszabályokkal, majd eltávolítja az első szabályt a szabálygyűjteményből a RemoveRuleByName hívási módszerrel a szabálygyűjtemény-objektumon.</span><span class="sxs-lookup"><span data-stu-id="6cbce-118">This example creates a new NAT rule collection with two rules and then removes the first rule from the rule collection by calling method RemoveRuleByName on the rule collection object.</span></span> <span data-ttu-id="6cbce-119">A RemoveRuleByName metódus szabályneve a kis- és</span><span class="sxs-lookup"><span data-stu-id="6cbce-119">The rule name for method RemoveRuleByName is case-insensitive.</span></span>

## <span data-ttu-id="6cbce-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6cbce-120">PARAMETERS</span></span>

### <span data-ttu-id="6cbce-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cbce-121">-DefaultProfile</span></span>
<span data-ttu-id="6cbce-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6cbce-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6cbce-123">-Name</span><span class="sxs-lookup"><span data-stu-id="6cbce-123">-Name</span></span>
<span data-ttu-id="6cbce-124">A NAT-szabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6cbce-124">Specifies the name of this NAT rule.</span></span> <span data-ttu-id="6cbce-125">A névnek egyedinek kell lennie egy szabálygyűjteményben.</span><span class="sxs-lookup"><span data-stu-id="6cbce-125">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="6cbce-126">-Priority</span><span class="sxs-lookup"><span data-stu-id="6cbce-126">-Priority</span></span>
<span data-ttu-id="6cbce-127">Megadja a szabály prioritását.</span><span class="sxs-lookup"><span data-stu-id="6cbce-127">Specifies the priority of this rule.</span></span> <span data-ttu-id="6cbce-128">A prioritás 100 és 65000 közötti szám.</span><span class="sxs-lookup"><span data-stu-id="6cbce-128">Priority is a number between 100 and 65000.</span></span> <span data-ttu-id="6cbce-129">Minél kisebb a szám, annál nagyobb a prioritás.</span><span class="sxs-lookup"><span data-stu-id="6cbce-129">The smaller the number, the bigger the priority.</span></span>

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

### <span data-ttu-id="6cbce-130">-Rule</span><span class="sxs-lookup"><span data-stu-id="6cbce-130">-Rule</span></span>
<span data-ttu-id="6cbce-131">Az ebben a gyűjteményben csoportosított szabályok listáját határozza meg.</span><span class="sxs-lookup"><span data-stu-id="6cbce-131">Specifies the list of rules to be grouped under this collection.</span></span>

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

### <span data-ttu-id="6cbce-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6cbce-132">-Confirm</span></span>
<span data-ttu-id="6cbce-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6cbce-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6cbce-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cbce-134">-WhatIf</span></span>
<span data-ttu-id="6cbce-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6cbce-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6cbce-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6cbce-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6cbce-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cbce-137">CommonParameters</span></span>
<span data-ttu-id="6cbce-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cbce-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cbce-139">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cbce-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cbce-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6cbce-140">INPUTS</span></span>

### <span data-ttu-id="6cbce-141">Nincs</span><span class="sxs-lookup"><span data-stu-id="6cbce-141">None</span></span>

## <span data-ttu-id="6cbce-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6cbce-142">OUTPUTS</span></span>

### <span data-ttu-id="6cbce-143">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="6cbce-143">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection</span></span>

## <span data-ttu-id="6cbce-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6cbce-144">NOTES</span></span>

## <span data-ttu-id="6cbce-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6cbce-145">RELATED LINKS</span></span>

[<span data-ttu-id="6cbce-146">New-AzFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="6cbce-146">New-AzFirewallNatRule</span></span>](./New-AzFirewallNatRule.md)

[<span data-ttu-id="6cbce-147">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="6cbce-147">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="6cbce-148">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="6cbce-148">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
