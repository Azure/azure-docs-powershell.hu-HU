---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedrulegroupoverride
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride.md
ms.openlocfilehash: 81b09a392464a004030a0798ea211db08a60a9f4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100146979"
---
# <span data-ttu-id="17798-101">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="17798-101">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>

## <span data-ttu-id="17798-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17798-102">SYNOPSIS</span></span>
<span data-ttu-id="17798-103">Létrehozza a RuleGroupOverride bejegyzést a ManagedRuleSets szolgáltatásban a tűzfal házirendhez.</span><span class="sxs-lookup"><span data-stu-id="17798-103">Creates RuleGroupOverride entry in ManagedRuleSets for the firewall policy.</span></span>

## <span data-ttu-id="17798-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="17798-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride -RuleGroupName <String>
 -Rule <PSApplicationGatewayFirewallPolicyManagedRuleOverride[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="17798-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="17798-105">DESCRIPTION</span></span>
<span data-ttu-id="17798-106">A **New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride** létrehoz egy ruleGroupOverride bejegyzést egy felügyeltRuleSetben tűzfal-házirendhez.</span><span class="sxs-lookup"><span data-stu-id="17798-106">The **New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride** creates a ruleGroupOverride entry in a managedRuleSet for a firewall policy.</span></span>

## <span data-ttu-id="17798-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="17798-107">EXAMPLES</span></span>

### <span data-ttu-id="17798-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="17798-108">Example 1</span></span>
```powershell
PS C:\> $overrideEntry = New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride -RuleGroupName $ruleName -Rules $rule1,$rule2
```

<span data-ttu-id="17798-109">Létrehoz egy RuleGroupOverride bejegyzést, amely a következő néven $ruleName és szabályok $rule 1, $rule 2.</span><span class="sxs-lookup"><span data-stu-id="17798-109">Creates a RuleGroupOverride entry with group name as $ruleName and Rules as $rule1, $rule2.</span></span> <span data-ttu-id="17798-110">Ugyanazt rendeli a $overrideEntry</span><span class="sxs-lookup"><span data-stu-id="17798-110">Assigns the same to $overrideEntry</span></span>

## <span data-ttu-id="17798-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="17798-111">PARAMETERS</span></span>

### <span data-ttu-id="17798-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17798-112">-DefaultProfile</span></span>
<span data-ttu-id="17798-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="17798-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17798-114">-Rule</span><span class="sxs-lookup"><span data-stu-id="17798-114">-Rule</span></span>
<span data-ttu-id="17798-115">Szabályok listája.</span><span class="sxs-lookup"><span data-stu-id="17798-115">List of Rules.</span></span>

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

### <span data-ttu-id="17798-116">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="17798-116">-RuleGroupName</span></span>
<span data-ttu-id="17798-117">Adja meg a ruleGroupName értéket egy felülbírálási RuleGroup bejegyzésben.</span><span class="sxs-lookup"><span data-stu-id="17798-117">Specify the ruleGroupName in a override RuleGroup entry.</span></span>

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

### <span data-ttu-id="17798-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17798-118">CommonParameters</span></span>
<span data-ttu-id="17798-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17798-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17798-120">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="17798-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17798-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="17798-121">INPUTS</span></span>

### <span data-ttu-id="17798-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="17798-122">None</span></span>

## <span data-ttu-id="17798-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="17798-123">OUTPUTS</span></span>

### <span data-ttu-id="17798-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="17798-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>

## <span data-ttu-id="17798-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="17798-125">NOTES</span></span>

## <span data-ttu-id="17798-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="17798-126">RELATED LINKS</span></span>
