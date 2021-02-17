---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleSet.md
ms.openlocfilehash: 3f4faec6b2af39f3386ec39e7df2e5bebcfe4277
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156938"
---
# <span data-ttu-id="30bb7-101">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="30bb7-101">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>

## <span data-ttu-id="30bb7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30bb7-102">SYNOPSIS</span></span>
<span data-ttu-id="30bb7-103">ManagedRuleSetet hoz létre a firewallPolicy számára</span><span class="sxs-lookup"><span data-stu-id="30bb7-103">Creates a ManagedRuleSet for the firewallPolicy</span></span>

## <span data-ttu-id="30bb7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="30bb7-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRuleSet -RuleSetType <String> -RuleSetVersion <String>
 [-RuleGroupOverride <PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30bb7-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="30bb7-105">DESCRIPTION</span></span>
<span data-ttu-id="30bb7-106">A **New-AzApplicationGatewayFirewallPolicyManagedRuleSet** létrehoz egy felügyelt szabályokat egy tűzfal-házirendhez.</span><span class="sxs-lookup"><span data-stu-id="30bb7-106">The **New-AzApplicationGatewayFirewallPolicyManagedRuleSet** creates a managed-rules for a firewall policy.</span></span>

## <span data-ttu-id="30bb7-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="30bb7-107">EXAMPLES</span></span>

### <span data-ttu-id="30bb7-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="30bb7-108">Example 1</span></span>
```powershell
PS C:\> $managedRuleSet = New-AzApplicationGatewayFirewallPolicyManagedRuleSet -RuleSetType $ruleSetType 
-RuleSetVersion $ruleSetVersion -RuleGroupOverrides $ruleGroupOverride1, $ruleGroupOverride2
```

<span data-ttu-id="30bb7-109">Létrehoz egy ManagedRuleSetet a ruleSetType típussal $ruleSetType, ruleSetVersion as $ruleSetVersion és RuleGroupOverrides mint egy teljes listára ($ruleGroupOverride 1, $ruleGroupOverride 2) az új ManagedRuleSet hozzá van rendelve $managedRuleSet</span><span class="sxs-lookup"><span data-stu-id="30bb7-109">Creates a ManagedRuleSet with ruleSetType as $ruleSetType, ruleSetVersion as $ruleSetVersion and RuleGroupOverrides as a list with entires as $ruleGroupOverride1, $ruleGroupOverride2 The new ManagedRuleSet is assigned to $managedRuleSet</span></span>

## <span data-ttu-id="30bb7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="30bb7-110">PARAMETERS</span></span>

### <span data-ttu-id="30bb7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30bb7-111">-DefaultProfile</span></span>
<span data-ttu-id="30bb7-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="30bb7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30bb7-113">-RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="30bb7-113">-RuleGroupOverride</span></span>
<span data-ttu-id="30bb7-114">Szabálycsoport felülbírálása.</span><span class="sxs-lookup"><span data-stu-id="30bb7-114">Rule Group Overrides.</span></span>

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

### <span data-ttu-id="30bb7-115">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="30bb7-115">-RuleSetType</span></span>
<span data-ttu-id="30bb7-116">A RuleSetType megadása felügyeltRuleSetben</span><span class="sxs-lookup"><span data-stu-id="30bb7-116">Specify the RuleSetType in a managedRuleSet</span></span>

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

### <span data-ttu-id="30bb7-117">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="30bb7-117">-RuleSetVersion</span></span>
<span data-ttu-id="30bb7-118">A RuleSetVersion megadása felügyeltRuleSetben</span><span class="sxs-lookup"><span data-stu-id="30bb7-118">Specify the RuleSetVersion in a managedRuleSet</span></span>

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

### <span data-ttu-id="30bb7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30bb7-119">CommonParameters</span></span>
<span data-ttu-id="30bb7-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30bb7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30bb7-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="30bb7-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30bb7-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="30bb7-122">INPUTS</span></span>

### <span data-ttu-id="30bb7-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="30bb7-123">None</span></span>

## <span data-ttu-id="30bb7-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="30bb7-124">OUTPUTS</span></span>

### <span data-ttu-id="30bb7-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="30bb7-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleSet</span></span>

## <span data-ttu-id="30bb7-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="30bb7-126">NOTES</span></span>

## <span data-ttu-id="30bb7-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="30bb7-127">RELATED LINKS</span></span>
