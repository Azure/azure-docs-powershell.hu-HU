---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleSet.md
ms.openlocfilehash: 3f4faec6b2af39f3386ec39e7df2e5bebcfe4277
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014812"
---
# <span data-ttu-id="36e18-101">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="36e18-101">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>

## <span data-ttu-id="36e18-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="36e18-102">SYNOPSIS</span></span>
<span data-ttu-id="36e18-103">ManagedRuleSet hoz létre a firewallPolicy</span><span class="sxs-lookup"><span data-stu-id="36e18-103">Creates a ManagedRuleSet for the firewallPolicy</span></span>

## <span data-ttu-id="36e18-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="36e18-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRuleSet -RuleSetType <String> -RuleSetVersion <String>
 [-RuleGroupOverride <PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36e18-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="36e18-105">DESCRIPTION</span></span>
<span data-ttu-id="36e18-106">A **New-AzApplicationGatewayFirewallPolicyManagedRuleSet** létrehoz egy felügyelt szabályokat a tűzfal házirendjéhez.</span><span class="sxs-lookup"><span data-stu-id="36e18-106">The **New-AzApplicationGatewayFirewallPolicyManagedRuleSet** creates a managed-rules for a firewall policy.</span></span>

## <span data-ttu-id="36e18-107">Példák</span><span class="sxs-lookup"><span data-stu-id="36e18-107">EXAMPLES</span></span>

### <span data-ttu-id="36e18-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="36e18-108">Example 1</span></span>
```powershell
PS C:\> $managedRuleSet = New-AzApplicationGatewayFirewallPolicyManagedRuleSet -RuleSetType $ruleSetType 
-RuleSetVersion $ruleSetVersion -RuleGroupOverrides $ruleGroupOverride1, $ruleGroupOverride2
```

<span data-ttu-id="36e18-109">Olyan ManagedRuleSet hoz létre, amelyben a $ruleSetType ruleSetType, az ruleSetVersion, a $ruleSetVersion és a RuleGroupOverrides a teljes $ruleGroupOverride 1 értékkel, $ruleGroupOverride 2 az új ManagedRuleSet $managedRuleSethoz van rendelve</span><span class="sxs-lookup"><span data-stu-id="36e18-109">Creates a ManagedRuleSet with ruleSetType as $ruleSetType, ruleSetVersion as $ruleSetVersion and RuleGroupOverrides as a list with entires as $ruleGroupOverride1, $ruleGroupOverride2 The new ManagedRuleSet is assigned to $managedRuleSet</span></span>

## <span data-ttu-id="36e18-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="36e18-110">PARAMETERS</span></span>

### <span data-ttu-id="36e18-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36e18-111">-DefaultProfile</span></span>
<span data-ttu-id="36e18-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="36e18-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36e18-113">-RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="36e18-113">-RuleGroupOverride</span></span>
<span data-ttu-id="36e18-114">A szabályok csoportjának felülírásai.</span><span class="sxs-lookup"><span data-stu-id="36e18-114">Rule Group Overrides.</span></span>

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

### <span data-ttu-id="36e18-115">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="36e18-115">-RuleSetType</span></span>
<span data-ttu-id="36e18-116">RuleSetType megadása egy managedRuleSet</span><span class="sxs-lookup"><span data-stu-id="36e18-116">Specify the RuleSetType in a managedRuleSet</span></span>

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

### <span data-ttu-id="36e18-117">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="36e18-117">-RuleSetVersion</span></span>
<span data-ttu-id="36e18-118">RuleSetVersion megadása egy managedRuleSet</span><span class="sxs-lookup"><span data-stu-id="36e18-118">Specify the RuleSetVersion in a managedRuleSet</span></span>

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

### <span data-ttu-id="36e18-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36e18-119">CommonParameters</span></span>
<span data-ttu-id="36e18-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="36e18-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36e18-121">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="36e18-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36e18-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="36e18-122">INPUTS</span></span>

### <span data-ttu-id="36e18-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="36e18-123">None</span></span>

## <span data-ttu-id="36e18-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="36e18-124">OUTPUTS</span></span>

### <span data-ttu-id="36e18-125">Microsoft. Azure. commands. Network. models. PSApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="36e18-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleSet</span></span>

## <span data-ttu-id="36e18-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="36e18-126">NOTES</span></span>

## <span data-ttu-id="36e18-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="36e18-127">RELATED LINKS</span></span>
