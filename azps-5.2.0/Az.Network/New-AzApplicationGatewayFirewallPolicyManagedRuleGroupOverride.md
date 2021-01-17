---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedrulegroupoverride
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride.md
ms.openlocfilehash: 81b09a392464a004030a0798ea211db08a60a9f4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98346601"
---
# <span data-ttu-id="89b65-101">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="89b65-101">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>

## <span data-ttu-id="89b65-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89b65-102">SYNOPSIS</span></span>
<span data-ttu-id="89b65-103">Létrehozza a RuleGroupOverride bejegyzést a ManagedRuleSets szolgáltatásban a tűzfal házirendhez.</span><span class="sxs-lookup"><span data-stu-id="89b65-103">Creates RuleGroupOverride entry in ManagedRuleSets for the firewall policy.</span></span>

## <span data-ttu-id="89b65-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="89b65-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride -RuleGroupName <String>
 -Rule <PSApplicationGatewayFirewallPolicyManagedRuleOverride[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="89b65-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="89b65-105">DESCRIPTION</span></span>
<span data-ttu-id="89b65-106">A **New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride** létrehoz egy ruleGroupOverride bejegyzést egy felügyeltRuleSetben tűzfal-házirendhez.</span><span class="sxs-lookup"><span data-stu-id="89b65-106">The **New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride** creates a ruleGroupOverride entry in a managedRuleSet for a firewall policy.</span></span>

## <span data-ttu-id="89b65-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="89b65-107">EXAMPLES</span></span>

### <span data-ttu-id="89b65-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="89b65-108">Example 1</span></span>
```powershell
PS C:\> $overrideEntry = New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride -RuleGroupName $ruleName -Rules $rule1,$rule2
```

<span data-ttu-id="89b65-109">Létrehoz egy RuleGroupOverride bejegyzést, amely a következő néven $ruleName és szabályok $rule 1, $rule 2.</span><span class="sxs-lookup"><span data-stu-id="89b65-109">Creates a RuleGroupOverride entry with group name as $ruleName and Rules as $rule1, $rule2.</span></span> <span data-ttu-id="89b65-110">Ugyanazt rendeli a $overrideEntry</span><span class="sxs-lookup"><span data-stu-id="89b65-110">Assigns the same to $overrideEntry</span></span>

## <span data-ttu-id="89b65-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="89b65-111">PARAMETERS</span></span>

### <span data-ttu-id="89b65-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89b65-112">-DefaultProfile</span></span>
<span data-ttu-id="89b65-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="89b65-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89b65-114">-Rule</span><span class="sxs-lookup"><span data-stu-id="89b65-114">-Rule</span></span>
<span data-ttu-id="89b65-115">Szabályok listája.</span><span class="sxs-lookup"><span data-stu-id="89b65-115">List of Rules.</span></span>

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

### <span data-ttu-id="89b65-116">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="89b65-116">-RuleGroupName</span></span>
<span data-ttu-id="89b65-117">Adja meg a ruleGroupName értéket egy felülbírálási RuleGroup bejegyzésben.</span><span class="sxs-lookup"><span data-stu-id="89b65-117">Specify the ruleGroupName in a override RuleGroup entry.</span></span>

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

### <span data-ttu-id="89b65-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89b65-118">CommonParameters</span></span>
<span data-ttu-id="89b65-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89b65-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89b65-120">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="89b65-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89b65-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="89b65-121">INPUTS</span></span>

### <span data-ttu-id="89b65-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="89b65-122">None</span></span>

## <span data-ttu-id="89b65-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="89b65-123">OUTPUTS</span></span>

### <span data-ttu-id="89b65-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="89b65-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>

## <span data-ttu-id="89b65-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="89b65-125">NOTES</span></span>

## <span data-ttu-id="89b65-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="89b65-126">RELATED LINKS</span></span>
