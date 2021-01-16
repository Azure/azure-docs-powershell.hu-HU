---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallapplicationrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRuleCollection.md
ms.openlocfilehash: 3e70aa93db8a230308687ce8b03d05d80ab3ab1a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98367553"
---
# <span data-ttu-id="cb9ce-101">New-AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="cb9ce-101">New-AzFirewallApplicationRuleCollection</span></span>

## <span data-ttu-id="cb9ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb9ce-102">SYNOPSIS</span></span>
<span data-ttu-id="cb9ce-103">Tűzfalalkalmazás-szabályok gyűjteményét hozza létre.</span><span class="sxs-lookup"><span data-stu-id="cb9ce-103">Creates a collection of Firewall application rules.</span></span>

## <span data-ttu-id="cb9ce-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cb9ce-104">SYNTAX</span></span>

```
New-AzFirewallApplicationRuleCollection -Name <String> -Priority <UInt32>
 -Rule <PSAzureFirewallApplicationRule[]> -ActionType <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb9ce-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cb9ce-105">DESCRIPTION</span></span>
<span data-ttu-id="cb9ce-106">A **New-AzFirewallApplicationRuleCollection** parancsmag tűzfalalkalmazási szabályok gyűjteményét hozza létre.</span><span class="sxs-lookup"><span data-stu-id="cb9ce-106">The **New-AzFirewallApplicationRuleCollection** cmdlet creates a collection of Firewall Application Rules.</span></span>

## <span data-ttu-id="cb9ce-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cb9ce-107">EXAMPLES</span></span>

### <span data-ttu-id="cb9ce-108">1. példa: Gyűjtemény létrehozása egyetlen s szabálysal</span><span class="sxs-lookup"><span data-stu-id="cb9ce-108">Example 1: Create a collection with one rule</span></span>
```powershell
$rule1 = New-AzFirewallApplicationRule -Name "httpsRule" -Protocol "https:443" -TargetFqdn "*" -SourceAddress "10.0.0.0"
New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 1000 -Rule $rule1 -ActionType "Allow"
```

<span data-ttu-id="cb9ce-109">Ez a példa létrehoz egy gyűjteményt egyetlen s szabálysal.</span><span class="sxs-lookup"><span data-stu-id="cb9ce-109">This example creates a collection with one rule.</span></span> <span data-ttu-id="cb9ce-110">Az $rule 1-ben meghatározott feltételeknek megfelelő összes forgalom engedélyezett lesz.</span><span class="sxs-lookup"><span data-stu-id="cb9ce-110">All traffic that matches the conditions identified in $rule1 will be allowed.</span></span>
<span data-ttu-id="cb9ce-111">Az első szabály a 10.0.0.0-s porton található összes HTTPS-forgalomra vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="cb9ce-111">The first rule is for all HTTPS traffic on port 443 from 10.0.0.0.</span></span> <span data-ttu-id="cb9ce-112">Ha egy másik, magasabb prioritású (kisebb számú) alkalmazásszabály-gyűjtemény is megfelel a $rule 1-ben azonosított forgalomnak, akkor a magasabb prioritású szabálygyűjteményre vonatkozó művelet lép életbe.</span><span class="sxs-lookup"><span data-stu-id="cb9ce-112">If there is another application rule collection with higher priority (smaller number) which also matches traffic identified in $rule1, the action of the rule collection with higher priority will take in effect instead.</span></span> 

### <span data-ttu-id="cb9ce-113">2. példa: Szabály hozzáadása szabálygyűjteményhez</span><span class="sxs-lookup"><span data-stu-id="cb9ce-113">Example 2: Add a rule to a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"

$rule2 = New-AzFirewallApplicationRule -Name R2 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" 
$ruleCollection.AddRule($rule2)
```

<span data-ttu-id="cb9ce-114">Ebben a példában egy új alkalmazásszabálygyűjteményt hoz létre egy s szabály alapján, majd hozzáad egy második szabályt a szabálygyűjteményhez az AddRule metódussal a szabálygyűjtemény-objektumon.</span><span class="sxs-lookup"><span data-stu-id="cb9ce-114">This example creates a new application rule collection with one rule and then adds a second rule to the rule collection using method AddRule on the rule collection object.</span></span> <span data-ttu-id="cb9ce-115">Az adott szabálygyűjteményben minden szabálynévnek egyedi névvel kell lennie, és a kis- és a nagy- és a kis</span><span class="sxs-lookup"><span data-stu-id="cb9ce-115">Each rule name in a given rule collection must have a unique name and is case insensitive.</span></span>

### <span data-ttu-id="cb9ce-116">3. példa: Szabály begyűjtése szabálygyűjteményből</span><span class="sxs-lookup"><span data-stu-id="cb9ce-116">Example 3: Get a rule from a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"
$getRule=$ruleCollection.GetRuleByName("r1")
```

<span data-ttu-id="cb9ce-117">Ebben a példában egy új alkalmazásszabálygyűjteményt hoz létre egy s szabály alapján, majd név szerint, a GetRuleByName hívási metódust kapja meg a szabálygyűjtemény-objektumon.</span><span class="sxs-lookup"><span data-stu-id="cb9ce-117">This example creates a new application rule collection with one rule and then gets the rule by name, calling method GetRuleByName on the rule collection object.</span></span> <span data-ttu-id="cb9ce-118">A GetRuleByName metódus szabályneve a kis- és</span><span class="sxs-lookup"><span data-stu-id="cb9ce-118">The rule name for method GetRuleByName is case-insensitive.</span></span>

### <span data-ttu-id="cb9ce-119">4. példa: Szabály eltávolítása szabálygyűjteményből</span><span class="sxs-lookup"><span data-stu-id="cb9ce-119">Example 4: Remove a rule from a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$rule2 = New-AzFirewallApplicationRule -Name R2 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1, $rule1 -ActionType "Allow"
$ruleCollection.RemoveRuleByName("r1")
```

<span data-ttu-id="cb9ce-120">Ez a példa létrehoz egy új alkalmazásszabálygyűjteményt két sszabályokkal, majd eltávolítja az első szabályt a szabálygyűjteményből a RemoveRuleByName hívási módszerrel a szabálygyűjtemény-objektumon.</span><span class="sxs-lookup"><span data-stu-id="cb9ce-120">This example creates a new application rule collection with two rules and then removes the first rule from the rule collection by calling method RemoveRuleByName on the rule collection object.</span></span> <span data-ttu-id="cb9ce-121">A RemoveRuleByName metódus szabályneve a kis- és</span><span class="sxs-lookup"><span data-stu-id="cb9ce-121">The rule name for method RemoveRuleByName is case-insensitive.</span></span>

## <span data-ttu-id="cb9ce-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cb9ce-122">PARAMETERS</span></span>

### <span data-ttu-id="cb9ce-123">-ActionType</span><span class="sxs-lookup"><span data-stu-id="cb9ce-123">-ActionType</span></span>
<span data-ttu-id="cb9ce-124">A szabálygyűjtemény művelete</span><span class="sxs-lookup"><span data-stu-id="cb9ce-124">The action of the rule collection</span></span>

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

### <span data-ttu-id="cb9ce-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb9ce-125">-DefaultProfile</span></span>
<span data-ttu-id="cb9ce-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cb9ce-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb9ce-127">-Name</span><span class="sxs-lookup"><span data-stu-id="cb9ce-127">-Name</span></span>
<span data-ttu-id="cb9ce-128">Az alkalmazásszabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cb9ce-128">Specifies the name of this application rule.</span></span> <span data-ttu-id="cb9ce-129">A névnek egyedinek kell lennie egy szabálygyűjteményben.</span><span class="sxs-lookup"><span data-stu-id="cb9ce-129">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="cb9ce-130">-Priority</span><span class="sxs-lookup"><span data-stu-id="cb9ce-130">-Priority</span></span>
<span data-ttu-id="cb9ce-131">Megadja a szabály prioritását.</span><span class="sxs-lookup"><span data-stu-id="cb9ce-131">Specifies the priority of this rule.</span></span> <span data-ttu-id="cb9ce-132">A prioritás 100 és 65000 közötti szám.</span><span class="sxs-lookup"><span data-stu-id="cb9ce-132">Priority is a number between 100 and 65000.</span></span> <span data-ttu-id="cb9ce-133">Minél kisebb a szám, annál nagyobb a prioritás.</span><span class="sxs-lookup"><span data-stu-id="cb9ce-133">The smaller the number, the bigger the priority.</span></span>

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

### <span data-ttu-id="cb9ce-134">-Rule</span><span class="sxs-lookup"><span data-stu-id="cb9ce-134">-Rule</span></span>
<span data-ttu-id="cb9ce-135">Az ebben a gyűjteményben csoportosított szabályok listáját határozza meg.</span><span class="sxs-lookup"><span data-stu-id="cb9ce-135">Specifies the list of rules to be grouped under this collection.</span></span>

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

### <span data-ttu-id="cb9ce-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cb9ce-136">-Confirm</span></span>
<span data-ttu-id="cb9ce-137">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="cb9ce-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb9ce-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb9ce-138">-WhatIf</span></span>
<span data-ttu-id="cb9ce-139">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="cb9ce-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb9ce-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cb9ce-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb9ce-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb9ce-141">CommonParameters</span></span>
<span data-ttu-id="cb9ce-142">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb9ce-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb9ce-143">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb9ce-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb9ce-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cb9ce-144">INPUTS</span></span>

### <span data-ttu-id="cb9ce-145">Nincs</span><span class="sxs-lookup"><span data-stu-id="cb9ce-145">None</span></span>

## <span data-ttu-id="cb9ce-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cb9ce-146">OUTPUTS</span></span>

### <span data-ttu-id="cb9ce-147">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="cb9ce-147">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection</span></span>

## <span data-ttu-id="cb9ce-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cb9ce-148">NOTES</span></span>

## <span data-ttu-id="cb9ce-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cb9ce-149">RELATED LINKS</span></span>

[<span data-ttu-id="cb9ce-150">New-AzFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="cb9ce-150">New-AzFirewallApplicationRule</span></span>](./New-AzFirewallApplicationRule.md)

[<span data-ttu-id="cb9ce-151">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="cb9ce-151">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="cb9ce-152">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="cb9ce-152">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
