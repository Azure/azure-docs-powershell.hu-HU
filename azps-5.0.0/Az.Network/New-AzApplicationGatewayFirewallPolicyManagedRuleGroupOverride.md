---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedrulegroupoverride
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride.md
ms.openlocfilehash: 81b09a392464a004030a0798ea211db08a60a9f4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186199"
---
# <span data-ttu-id="63211-101">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="63211-101">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>

## <span data-ttu-id="63211-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="63211-102">SYNOPSIS</span></span>
<span data-ttu-id="63211-103">RuleGroupOverride-bejegyzést hoz létre a ManagedRuleSets a tűzfal házirendjéhez.</span><span class="sxs-lookup"><span data-stu-id="63211-103">Creates RuleGroupOverride entry in ManagedRuleSets for the firewall policy.</span></span>

## <span data-ttu-id="63211-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="63211-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride -RuleGroupName <String>
 -Rule <PSApplicationGatewayFirewallPolicyManagedRuleOverride[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="63211-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="63211-105">DESCRIPTION</span></span>
<span data-ttu-id="63211-106">A **New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride** létrehoz egy ruleGroupOverride bejegyzést egy tűzfal-házirend managedRuleSet.</span><span class="sxs-lookup"><span data-stu-id="63211-106">The **New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride** creates a ruleGroupOverride entry in a managedRuleSet for a firewall policy.</span></span>

## <span data-ttu-id="63211-107">Példák</span><span class="sxs-lookup"><span data-stu-id="63211-107">EXAMPLES</span></span>

### <span data-ttu-id="63211-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="63211-108">Example 1</span></span>
```powershell
PS C:\> $overrideEntry = New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride -RuleGroupName $ruleName -Rules $rule1,$rule2
```

<span data-ttu-id="63211-109">Egy RuleGroupOverride-bejegyzést hoz létre, amelyben a csoport neve $ruleName és a szabályok $rule 1, $rule 2.</span><span class="sxs-lookup"><span data-stu-id="63211-109">Creates a RuleGroupOverride entry with group name as $ruleName and Rules as $rule1, $rule2.</span></span> <span data-ttu-id="63211-110">A $overrideEntry</span><span class="sxs-lookup"><span data-stu-id="63211-110">Assigns the same to $overrideEntry</span></span>

## <span data-ttu-id="63211-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="63211-111">PARAMETERS</span></span>

### <span data-ttu-id="63211-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63211-112">-DefaultProfile</span></span>
<span data-ttu-id="63211-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="63211-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63211-114">-Szabály</span><span class="sxs-lookup"><span data-stu-id="63211-114">-Rule</span></span>
<span data-ttu-id="63211-115">Szabályok listája.</span><span class="sxs-lookup"><span data-stu-id="63211-115">List of Rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleOverride[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63211-116">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="63211-116">-RuleGroupName</span></span>
<span data-ttu-id="63211-117">Adja meg a ruleGroupName a felülírás RuleGroup-bejegyzésben.</span><span class="sxs-lookup"><span data-stu-id="63211-117">Specify the ruleGroupName in a override RuleGroup entry.</span></span>

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

### <span data-ttu-id="63211-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63211-118">CommonParameters</span></span>
<span data-ttu-id="63211-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="63211-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63211-120">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="63211-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63211-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="63211-121">INPUTS</span></span>

### <span data-ttu-id="63211-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="63211-122">None</span></span>

## <span data-ttu-id="63211-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="63211-123">OUTPUTS</span></span>

### <span data-ttu-id="63211-124">Microsoft. Azure. commands. Network. models. PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="63211-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>

## <span data-ttu-id="63211-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="63211-125">NOTES</span></span>

## <span data-ttu-id="63211-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="63211-126">RELATED LINKS</span></span>
