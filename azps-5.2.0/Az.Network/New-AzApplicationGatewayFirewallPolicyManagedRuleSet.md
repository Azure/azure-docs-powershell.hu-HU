---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleSet.md
ms.openlocfilehash: 3f4faec6b2af39f3386ec39e7df2e5bebcfe4277
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98346565"
---
# <span data-ttu-id="26d8b-101">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="26d8b-101">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>

## <span data-ttu-id="26d8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26d8b-102">SYNOPSIS</span></span>
<span data-ttu-id="26d8b-103">ManagedRuleSetet hoz létre a firewallPolicy szolgáltatáshoz</span><span class="sxs-lookup"><span data-stu-id="26d8b-103">Creates a ManagedRuleSet for the firewallPolicy</span></span>

## <span data-ttu-id="26d8b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="26d8b-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRuleSet -RuleSetType <String> -RuleSetVersion <String>
 [-RuleGroupOverride <PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26d8b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="26d8b-105">DESCRIPTION</span></span>
<span data-ttu-id="26d8b-106">A **New-AzApplicationGatewayFirewallPolicyManagedRuleSet** létrehoz egy felügyelt szabályokat egy tűzfal-házirendhez.</span><span class="sxs-lookup"><span data-stu-id="26d8b-106">The **New-AzApplicationGatewayFirewallPolicyManagedRuleSet** creates a managed-rules for a firewall policy.</span></span>

## <span data-ttu-id="26d8b-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="26d8b-107">EXAMPLES</span></span>

### <span data-ttu-id="26d8b-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="26d8b-108">Example 1</span></span>
```powershell
PS C:\> $managedRuleSet = New-AzApplicationGatewayFirewallPolicyManagedRuleSet -RuleSetType $ruleSetType 
-RuleSetVersion $ruleSetVersion -RuleGroupOverrides $ruleGroupOverride1, $ruleGroupOverride2
```

<span data-ttu-id="26d8b-109">Létrehozza a "RuleRuleSetType" tulajdonságot $ruleSetType, a ruleSetVersion as $ruleSetVersion és a RuleGroupOverrides csoportot teljes listaként ( $ruleGroupOverride 1, $ruleGroupOverride 2) az új ManagedRuleSet hozzárendeli a $managedRuleSet</span><span class="sxs-lookup"><span data-stu-id="26d8b-109">Creates a ManagedRuleSet with ruleSetType as $ruleSetType, ruleSetVersion as $ruleSetVersion and RuleGroupOverrides as a list with entires as $ruleGroupOverride1, $ruleGroupOverride2 The new ManagedRuleSet is assigned to $managedRuleSet</span></span>

## <span data-ttu-id="26d8b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="26d8b-110">PARAMETERS</span></span>

### <span data-ttu-id="26d8b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26d8b-111">-DefaultProfile</span></span>
<span data-ttu-id="26d8b-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="26d8b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26d8b-113">-RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="26d8b-113">-RuleGroupOverride</span></span>
<span data-ttu-id="26d8b-114">Szabálycsoport felülbírálása.</span><span class="sxs-lookup"><span data-stu-id="26d8b-114">Rule Group Overrides.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26d8b-115">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="26d8b-115">-RuleSetType</span></span>
<span data-ttu-id="26d8b-116">A RuleSetType megadása felügyeltRuleSetben</span><span class="sxs-lookup"><span data-stu-id="26d8b-116">Specify the RuleSetType in a managedRuleSet</span></span>

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

### <span data-ttu-id="26d8b-117">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="26d8b-117">-RuleSetVersion</span></span>
<span data-ttu-id="26d8b-118">A RuleSetVersion megadása felügyeltRuleSetben</span><span class="sxs-lookup"><span data-stu-id="26d8b-118">Specify the RuleSetVersion in a managedRuleSet</span></span>

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

### <span data-ttu-id="26d8b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26d8b-119">CommonParameters</span></span>
<span data-ttu-id="26d8b-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26d8b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26d8b-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="26d8b-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26d8b-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="26d8b-122">INPUTS</span></span>

### <span data-ttu-id="26d8b-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="26d8b-123">None</span></span>

## <span data-ttu-id="26d8b-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="26d8b-124">OUTPUTS</span></span>

### <span data-ttu-id="26d8b-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="26d8b-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleSet</span></span>

## <span data-ttu-id="26d8b-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="26d8b-126">NOTES</span></span>

## <span data-ttu-id="26d8b-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="26d8b-127">RELATED LINKS</span></span>
