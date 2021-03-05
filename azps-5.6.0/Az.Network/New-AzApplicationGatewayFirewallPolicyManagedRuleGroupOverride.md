---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedrulegroupoverride
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride.md
ms.openlocfilehash: 6b105ab242f9ffb64d1d523cad5930c48714c724
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001158"
---
# <span data-ttu-id="e2bb1-101">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="e2bb1-101">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>

## <span data-ttu-id="e2bb1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2bb1-102">SYNOPSIS</span></span>
<span data-ttu-id="e2bb1-103">Létrehozza a RuleGroupOverride bejegyzést a ManagedRuleSets szolgáltatásban a tűzfal házirendhez.</span><span class="sxs-lookup"><span data-stu-id="e2bb1-103">Creates RuleGroupOverride entry in ManagedRuleSets for the firewall policy.</span></span>

## <span data-ttu-id="e2bb1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e2bb1-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride -RuleGroupName <String>
 -Rule <PSApplicationGatewayFirewallPolicyManagedRuleOverride[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e2bb1-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e2bb1-105">DESCRIPTION</span></span>
<span data-ttu-id="e2bb1-106">A **New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride** létrehoz egy ruleGroupOverride bejegyzést egy felügyeltRuleSetben tűzfal-házirendhez.</span><span class="sxs-lookup"><span data-stu-id="e2bb1-106">The **New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride** creates a ruleGroupOverride entry in a managedRuleSet for a firewall policy.</span></span>

## <span data-ttu-id="e2bb1-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e2bb1-107">EXAMPLES</span></span>

### <span data-ttu-id="e2bb1-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="e2bb1-108">Example 1</span></span>
```powershell
PS C:\> $overrideEntry = New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride -RuleGroupName $ruleName -Rules $rule1,$rule2
```

<span data-ttu-id="e2bb1-109">Létrehoz egy RuleGroupOverride bejegyzést, amely a következő néven $ruleName és szabályok $rule 1, $rule 2.</span><span class="sxs-lookup"><span data-stu-id="e2bb1-109">Creates a RuleGroupOverride entry with group name as $ruleName and Rules as $rule1, $rule2.</span></span> <span data-ttu-id="e2bb1-110">Ugyanazt rendeli a $overrideEntry</span><span class="sxs-lookup"><span data-stu-id="e2bb1-110">Assigns the same to $overrideEntry</span></span>

## <span data-ttu-id="e2bb1-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e2bb1-111">PARAMETERS</span></span>

### <span data-ttu-id="e2bb1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2bb1-112">-DefaultProfile</span></span>
<span data-ttu-id="e2bb1-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e2bb1-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2bb1-114">-Rule</span><span class="sxs-lookup"><span data-stu-id="e2bb1-114">-Rule</span></span>
<span data-ttu-id="e2bb1-115">Szabályok listája.</span><span class="sxs-lookup"><span data-stu-id="e2bb1-115">List of Rules.</span></span>

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

### <span data-ttu-id="e2bb1-116">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="e2bb1-116">-RuleGroupName</span></span>
<span data-ttu-id="e2bb1-117">Adja meg a ruleGroupName értéket egy felülbírálási RuleGroup bejegyzésben.</span><span class="sxs-lookup"><span data-stu-id="e2bb1-117">Specify the ruleGroupName in a override RuleGroup entry.</span></span>

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

### <span data-ttu-id="e2bb1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2bb1-118">CommonParameters</span></span>
<span data-ttu-id="e2bb1-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2bb1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2bb1-120">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e2bb1-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2bb1-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e2bb1-121">INPUTS</span></span>

### <span data-ttu-id="e2bb1-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="e2bb1-122">None</span></span>

## <span data-ttu-id="e2bb1-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e2bb1-123">OUTPUTS</span></span>

### <span data-ttu-id="e2bb1-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="e2bb1-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>

## <span data-ttu-id="e2bb1-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e2bb1-125">NOTES</span></span>

## <span data-ttu-id="e2bb1-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e2bb1-126">RELATED LINKS</span></span>
