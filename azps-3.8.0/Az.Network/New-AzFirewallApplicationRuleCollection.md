---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallapplicationrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRuleCollection.md
ms.openlocfilehash: edf783daa552cee1de48f0ea4992f28d79a23e24
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845001"
---
# <span data-ttu-id="c29cf-101">New-AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="c29cf-101">New-AzFirewallApplicationRuleCollection</span></span>

## <span data-ttu-id="c29cf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c29cf-102">SYNOPSIS</span></span>
<span data-ttu-id="c29cf-103">Tűzfal-alkalmazási szabályok gyűjteményét hozza létre.</span><span class="sxs-lookup"><span data-stu-id="c29cf-103">Creates a collection of Firewall application rules.</span></span>

## <span data-ttu-id="c29cf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c29cf-104">SYNTAX</span></span>

```
New-AzFirewallApplicationRuleCollection -Name <String> -Priority <UInt32>
 -Rule <PSAzureFirewallApplicationRule[]> -ActionType <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c29cf-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c29cf-105">DESCRIPTION</span></span>
<span data-ttu-id="c29cf-106">A **New-AzFirewallApplicationRuleCollection** parancsmag egy tűzfal-alkalmazási szabályok gyűjteményét hozza létre.</span><span class="sxs-lookup"><span data-stu-id="c29cf-106">The **New-AzFirewallApplicationRuleCollection** cmdlet creates a collection of Firewall Application Rules.</span></span>

## <span data-ttu-id="c29cf-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c29cf-107">EXAMPLES</span></span>

### <span data-ttu-id="c29cf-108">1: gyűjtemény létrehozása egyetlen szabállyal</span><span class="sxs-lookup"><span data-stu-id="c29cf-108">1:  Create a collection with one rule</span></span>
```
$rule1 = New-AzFirewallApplicationRule -Name "httpsRule" -Protocol "https:443" -TargetFqdn "*" -SourceAddress "10.0.0.0"
New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 1000 -Rule $rule1 -ActionType "Allow"
```

<span data-ttu-id="c29cf-109">Ebben a példában egy-egy szabályt tartalmazó gyűjtemény jön létre.</span><span class="sxs-lookup"><span data-stu-id="c29cf-109">This example creates a collection with one rule.</span></span> <span data-ttu-id="c29cf-110">Az összes olyan forgalom, amely megfelel az 1. $ruleben meghatározott feltételeknek, engedélyezve lesz.</span><span class="sxs-lookup"><span data-stu-id="c29cf-110">All traffic that matches the conditions identified in $rule1 will be allowed.</span></span>
<span data-ttu-id="c29cf-111">Az első szabály az, hogy az 443-ös porton az összes HTTPS-forgalomra a 10.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="c29cf-111">The first rule is for all HTTPS traffic on port 443 from 10.0.0.0.</span></span> <span data-ttu-id="c29cf-112">Ha egy másik alkalmazási szabály-gyűjtemény magasabb prioritással (kisebb számmal) rendelkezik, amely a $rule 1-ben azonosított forgalomra is érvényes, akkor a magasabb prioritású szabály-gyűjteményben lévő műveletek inkább a megfelelő módon jelennek meg.</span><span class="sxs-lookup"><span data-stu-id="c29cf-112">If there is another application rule collection with higher priority (smaller number) which also matches traffic identified in $rule1, the action of the rule collection with higher priority will take in effect instead.</span></span> 

### <span data-ttu-id="c29cf-113">2: szabály hozzáadása egy szabály-gyűjteményhez</span><span class="sxs-lookup"><span data-stu-id="c29cf-113">2:  Add a rule to a rule collection</span></span>
```
$rule1 = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"

$rule2 = New-AzFirewallApplicationRule -Name R2 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" 
$ruleCollection.AddRule($rule2)
```

<span data-ttu-id="c29cf-114">Ebben a példában egy új alkalmazási szabály gyűjteményét hozza létre egy szabállyal, majd egy második szabályt szúr be a szabály-gyűjteménybe a AddRule metódus segítségével.</span><span class="sxs-lookup"><span data-stu-id="c29cf-114">This example creates a new application rule collection with one rule and then adds a second rule to the rule collection using method AddRule on the rule collection object.</span></span> <span data-ttu-id="c29cf-115">A megadott szabálygyűjtemény minden szabályának egyedi névvel kell rendelkeznie, és a kis-és nagybetűk megkülönböztetését is megadhatja.</span><span class="sxs-lookup"><span data-stu-id="c29cf-115">Each rule name in a given rule collection must have a unique name and is case insensitive.</span></span>

### <span data-ttu-id="c29cf-116">3: szabály kérése egy szabály-gyűjteményből</span><span class="sxs-lookup"><span data-stu-id="c29cf-116">3:  Get a rule from a rule collection</span></span>
```
$rule1 = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"
$getRule=$ruleCollection.GetRuleByName("r1")
```

<span data-ttu-id="c29cf-117">Ebben a példában egy új alkalmazási szabály gyűjteményét hozza létre egy szabállyal, majd a szabályt név szerint, a hívási módszer GetRuleByName a szabály-gyűjtemény objektumon kapja.</span><span class="sxs-lookup"><span data-stu-id="c29cf-117">This example creates a new application rule collection with one rule and then gets the rule by name, calling method GetRuleByName on the rule collection object.</span></span> <span data-ttu-id="c29cf-118">A GetRuleByName metódus szabályának neve megkülönbözteti a kis-és nagybetűket.</span><span class="sxs-lookup"><span data-stu-id="c29cf-118">The rule name for method GetRuleByName is case-insensitive.</span></span>

### <span data-ttu-id="c29cf-119">4: szabály eltávolítása a szabályok gyűjteményéből</span><span class="sxs-lookup"><span data-stu-id="c29cf-119">4:  Remove a rule from a rule collection</span></span>
```
$rule1 = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$rule2 = New-AzFirewallApplicationRule -Name R2 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1, $rule1 -ActionType "Allow"
$ruleCollection.RemoveRuleByName("r1")
```

<span data-ttu-id="c29cf-120">Ebben a példában egy új alkalmazás-szabály gyűjteményt hoz létre két szabállyal, majd eltávolítja az első szabályt a szabály gyűjteményből a RemoveRuleByName metódust.</span><span class="sxs-lookup"><span data-stu-id="c29cf-120">This example creates a new application rule collection with two rules and then removes the first rule from the rule collection by calling method RemoveRuleByName on the rule collection object.</span></span> <span data-ttu-id="c29cf-121">A RemoveRuleByName metódus szabályának neve megkülönbözteti a kis-és nagybetűket.</span><span class="sxs-lookup"><span data-stu-id="c29cf-121">The rule name for method RemoveRuleByName is case-insensitive.</span></span>

## <span data-ttu-id="c29cf-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c29cf-122">PARAMETERS</span></span>

### <span data-ttu-id="c29cf-123">-ActionType</span><span class="sxs-lookup"><span data-stu-id="c29cf-123">-ActionType</span></span>
<span data-ttu-id="c29cf-124">A szabály-gyűjtemény lépései</span><span class="sxs-lookup"><span data-stu-id="c29cf-124">The action of the rule collection</span></span>

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

### <span data-ttu-id="c29cf-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c29cf-125">-DefaultProfile</span></span>
<span data-ttu-id="c29cf-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c29cf-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c29cf-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c29cf-127">-Name</span></span>
<span data-ttu-id="c29cf-128">Az alkalmazási szabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c29cf-128">Specifies the name of this application rule.</span></span> <span data-ttu-id="c29cf-129">A névnek egyedinek kell lennie egy szabály-gyűjteményen belül.</span><span class="sxs-lookup"><span data-stu-id="c29cf-129">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="c29cf-130">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="c29cf-130">-Priority</span></span>
<span data-ttu-id="c29cf-131">A szabály prioritását adja meg.</span><span class="sxs-lookup"><span data-stu-id="c29cf-131">Specifies the priority of this rule.</span></span> <span data-ttu-id="c29cf-132">A prioritás az 100 és az 65000 közötti szám.</span><span class="sxs-lookup"><span data-stu-id="c29cf-132">Priority is a number between 100 and 65000.</span></span> <span data-ttu-id="c29cf-133">Minél kisebb a szám, annál nagyobb a prioritás.</span><span class="sxs-lookup"><span data-stu-id="c29cf-133">The smaller the number, the bigger the priority.</span></span>

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

### <span data-ttu-id="c29cf-134">-Szabály</span><span class="sxs-lookup"><span data-stu-id="c29cf-134">-Rule</span></span>
<span data-ttu-id="c29cf-135">Az ebben a gyűjteményben csoportosítani kívánt szabályok listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c29cf-135">Specifies the list of rules to be grouped under this collection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c29cf-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c29cf-136">-Confirm</span></span>
<span data-ttu-id="c29cf-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c29cf-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c29cf-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c29cf-138">-WhatIf</span></span>
<span data-ttu-id="c29cf-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c29cf-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c29cf-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c29cf-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c29cf-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c29cf-141">CommonParameters</span></span>
<span data-ttu-id="c29cf-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c29cf-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c29cf-143">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c29cf-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c29cf-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c29cf-144">INPUTS</span></span>

### <span data-ttu-id="c29cf-145">Nincs</span><span class="sxs-lookup"><span data-stu-id="c29cf-145">None</span></span>

## <span data-ttu-id="c29cf-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c29cf-146">OUTPUTS</span></span>

### <span data-ttu-id="c29cf-147">Microsoft. Azure. commands. Network. models. PSAzureFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="c29cf-147">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection</span></span>

## <span data-ttu-id="c29cf-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c29cf-148">NOTES</span></span>

## <span data-ttu-id="c29cf-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c29cf-149">RELATED LINKS</span></span>

[<span data-ttu-id="c29cf-150">Új – AzFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="c29cf-150">New-AzFirewallApplicationRule</span></span>](./New-AzFirewallApplicationRule.md)

[<span data-ttu-id="c29cf-151">Új – AzFirewall</span><span class="sxs-lookup"><span data-stu-id="c29cf-151">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="c29cf-152">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="c29cf-152">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
