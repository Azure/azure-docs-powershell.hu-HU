---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermfirewallapplicationrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallApplicationRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallApplicationRuleCollection.md
ms.openlocfilehash: e5fbad2b63213af972260948439984754e9eaa3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680325"
---
# <span data-ttu-id="7802a-101">New-AzureRmFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="7802a-101">New-AzureRmFirewallApplicationRuleCollection</span></span>

## <span data-ttu-id="7802a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7802a-102">SYNOPSIS</span></span>
<span data-ttu-id="7802a-103">Tűzfal-alkalmazási szabályok gyűjteményét hozza létre.</span><span class="sxs-lookup"><span data-stu-id="7802a-103">Creates a collection of Firewall application rules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7802a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7802a-104">SYNTAX</span></span>

```
New-AzureRmFirewallApplicationRuleCollection -Name <String> -Priority <UInt32>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRule]>
 -ActionType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7802a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7802a-105">DESCRIPTION</span></span>
<span data-ttu-id="7802a-106">A **New-AzureRmFirewallApplicationRuleCollection** parancsmag egy tűzfal-alkalmazási szabályok gyűjteményét hozza létre.</span><span class="sxs-lookup"><span data-stu-id="7802a-106">The **New-AzureRmFirewallApplicationRuleCollection** cmdlet creates a collection of Firewall Application Rules.</span></span>

## <span data-ttu-id="7802a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7802a-107">EXAMPLES</span></span>

### <span data-ttu-id="7802a-108">1: gyűjtemény létrehozása egyetlen szabállyal</span><span class="sxs-lookup"><span data-stu-id="7802a-108">1:  Create a collection with one rule</span></span>
```
$rule1 = New-AzureRmFirewallApplicationRule -Name "httpsRule" -Protocol "https:443" -TargetFqdn "*" -SourceAddress "10.0.0.0"
New-AzureRmFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 1000 -Rule $rule1 -ActionType "Allow"
```

<span data-ttu-id="7802a-109">Ebben a példában egy-egy szabályt tartalmazó gyűjtemény jön létre.</span><span class="sxs-lookup"><span data-stu-id="7802a-109">This example creates a collection with one rule.</span></span> <span data-ttu-id="7802a-110">Az összes olyan forgalom, amely megfelel az 1. $ruleben meghatározott feltételeknek, engedélyezve lesz.</span><span class="sxs-lookup"><span data-stu-id="7802a-110">All traffic that matches the conditions identified in $rule1 will be allowed.</span></span>
<span data-ttu-id="7802a-111">Az első szabály az, hogy az 443-ös porton az összes HTTPS-forgalomra a 10.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="7802a-111">The first rule is for all HTTPS traffic on port 443 from 10.0.0.0.</span></span> <span data-ttu-id="7802a-112">Ha egy másik alkalmazási szabály-gyűjtemény magasabb prioritással (kisebb számmal) rendelkezik, amely a $rule 1-ben azonosított forgalomra is érvényes, akkor a magasabb prioritású szabály-gyűjteményben lévő műveletek inkább a megfelelő módon jelennek meg.</span><span class="sxs-lookup"><span data-stu-id="7802a-112">If there is another application rule collection with higher priority (smaller number) which also matches traffic identified in $rule1, the action of the rule collection with higher priority will take in effect instead.</span></span> 

### <span data-ttu-id="7802a-113">2: szabály hozzáadása egy szabály-gyűjteményhez</span><span class="sxs-lookup"><span data-stu-id="7802a-113">2:  Add a rule to a rule collection</span></span>
```
$rule1 = New-AzureRmFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$ruleCollection = New-AzureRmFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"

$rule2 = New-AzureRmFirewallApplicationRule -Name R2 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" 
$ruleCollection.AddRule($rule2)
```

<span data-ttu-id="7802a-114">Ebben a példában egy új alkalmazási szabály gyűjteményét hozza létre egy szabállyal, majd egy második szabályt szúr be a szabály-gyűjteménybe a AddRule metódus segítségével.</span><span class="sxs-lookup"><span data-stu-id="7802a-114">This example creates a new application rule collection with one rule and then adds a second rule to the rule collection using method AddRule on the rule collection object.</span></span> <span data-ttu-id="7802a-115">A megadott szabálygyűjtemény minden szabályának egyedi névvel kell rendelkeznie, és a kis-és nagybetűk megkülönböztetését is megadhatja.</span><span class="sxs-lookup"><span data-stu-id="7802a-115">Each rule name in a given rule collection must have a unique name and is case insensitive.</span></span>

### <span data-ttu-id="7802a-116">3: szabály kérése egy szabály-gyűjteményből</span><span class="sxs-lookup"><span data-stu-id="7802a-116">3:  Get a rule from a rule collection</span></span>
```
$rule1 = New-AzureRmFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$ruleCollection = New-AzureRmFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"
$getRule=$ruleCollection.GetRuleByName("r1")
```

<span data-ttu-id="7802a-117">Ebben a példában egy új alkalmazási szabály gyűjteményét hozza létre egy szabállyal, majd a szabályt név szerint, a hívási módszer GetRuleByName a szabály-gyűjtemény objektumon kapja.</span><span class="sxs-lookup"><span data-stu-id="7802a-117">This example creates a new application rule collection with one rule and then gets the rule by name, calling method GetRuleByName on the rule collection object.</span></span> <span data-ttu-id="7802a-118">A GetRuleByName metódus szabályának neve megkülönbözteti a kis-és nagybetűket.</span><span class="sxs-lookup"><span data-stu-id="7802a-118">The rule name for method GetRuleByName is case-insensitive.</span></span>

### <span data-ttu-id="7802a-119">4: szabály eltávolítása a szabályok gyűjteményéből</span><span class="sxs-lookup"><span data-stu-id="7802a-119">4:  Remove a rule from a rule collection</span></span>
```
$rule1 = New-AzureRmFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$rule2 = New-AzureRmFirewallApplicationRule -Name R2 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" 
$ruleCollection = New-AzureRmFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1, $rule1 -ActionType "Allow"
$ruleCollection.RemoveRuleByName("r1")
```

<span data-ttu-id="7802a-120">Ebben a példában egy új alkalmazás-szabály gyűjteményt hoz létre két szabállyal, majd eltávolítja az első szabályt a szabály gyűjteményből a RemoveRuleByName metódust.</span><span class="sxs-lookup"><span data-stu-id="7802a-120">This example creates a new application rule collection with two rules and then removes the first rule from the rule collection by calling method RemoveRuleByName on the rule collection object.</span></span> <span data-ttu-id="7802a-121">A RemoveRuleByName metódus szabályának neve megkülönbözteti a kis-és nagybetűket.</span><span class="sxs-lookup"><span data-stu-id="7802a-121">The rule name for method RemoveRuleByName is case-insensitive.</span></span>

## <span data-ttu-id="7802a-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7802a-122">PARAMETERS</span></span>

### <span data-ttu-id="7802a-123">-ActionType</span><span class="sxs-lookup"><span data-stu-id="7802a-123">-ActionType</span></span>
<span data-ttu-id="7802a-124">A szabály-gyűjtemény lépései</span><span class="sxs-lookup"><span data-stu-id="7802a-124">The action of the rule collection</span></span>

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

### <span data-ttu-id="7802a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7802a-125">-DefaultProfile</span></span>
<span data-ttu-id="7802a-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7802a-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7802a-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7802a-127">-Name</span></span>
<span data-ttu-id="7802a-128">Az alkalmazási szabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7802a-128">Specifies the name of this application rule.</span></span> <span data-ttu-id="7802a-129">A névnek egyedinek kell lennie egy szabály-gyűjteményen belül.</span><span class="sxs-lookup"><span data-stu-id="7802a-129">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="7802a-130">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="7802a-130">-Priority</span></span>
<span data-ttu-id="7802a-131">A szabály prioritását adja meg.</span><span class="sxs-lookup"><span data-stu-id="7802a-131">Specifies the priority of this rule.</span></span> <span data-ttu-id="7802a-132">A prioritás az 100 és az 65000 közötti szám.</span><span class="sxs-lookup"><span data-stu-id="7802a-132">Priority is a number between 100 and 65000.</span></span> <span data-ttu-id="7802a-133">Minél kisebb a szám, annál nagyobb a prioritás.</span><span class="sxs-lookup"><span data-stu-id="7802a-133">The smaller the number, the bigger the priority.</span></span>

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

### <span data-ttu-id="7802a-134">-Szabály</span><span class="sxs-lookup"><span data-stu-id="7802a-134">-Rule</span></span>
<span data-ttu-id="7802a-135">Az ebben a gyűjteményben csoportosítani kívánt szabályok listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7802a-135">Specifies the list of rules to be grouped under this collection.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRule]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7802a-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7802a-136">-Confirm</span></span>
<span data-ttu-id="7802a-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7802a-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7802a-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7802a-138">-WhatIf</span></span>
<span data-ttu-id="7802a-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7802a-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7802a-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7802a-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7802a-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7802a-141">CommonParameters</span></span>
<span data-ttu-id="7802a-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7802a-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7802a-143">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7802a-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7802a-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7802a-144">INPUTS</span></span>

### <span data-ttu-id="7802a-145">Nincs</span><span class="sxs-lookup"><span data-stu-id="7802a-145">None</span></span>
<span data-ttu-id="7802a-146">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="7802a-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7802a-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7802a-147">OUTPUTS</span></span>

### <span data-ttu-id="7802a-148">Microsoft. Azure. commands. Network. models. PSFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="7802a-148">Microsoft.Azure.Commands.Network.Models.PSFirewallApplicationRuleCollection</span></span>

## <span data-ttu-id="7802a-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7802a-149">NOTES</span></span>

## <span data-ttu-id="7802a-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7802a-150">RELATED LINKS</span></span>

[<span data-ttu-id="7802a-151">Új – AzureRmFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="7802a-151">New-AzureRmFirewallApplicationRule</span></span>](./New-AzureRmFirewallApplicationRule.md)

[<span data-ttu-id="7802a-152">Új – AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="7802a-152">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)

[<span data-ttu-id="7802a-153">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="7802a-153">Get-AzureRmFirewall</span></span>](./Get-AzureRmFirewall.md)
