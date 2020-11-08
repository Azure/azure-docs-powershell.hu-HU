---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedruleoverride
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleOverride.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleOverride.md
ms.openlocfilehash: a3e057b8fbf6b04f48936b2aa96e9696964e5061
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194281"
---
# <span data-ttu-id="3e958-101">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="3e958-101">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>

## <span data-ttu-id="3e958-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3e958-102">SYNOPSIS</span></span>
<span data-ttu-id="3e958-103">ManagedRuleOverride-bejegyzés létrehozása a RuleGroupOverrideGroup bejegyzéshez.</span><span class="sxs-lookup"><span data-stu-id="3e958-103">Creates a managedRuleOverride entry for RuleGroupOverrideGroup entry.</span></span>

## <span data-ttu-id="3e958-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3e958-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRuleOverride -RuleId <String> [-State <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e958-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3e958-105">DESCRIPTION</span></span>
<span data-ttu-id="3e958-106">A **New-AzApplicationGatewayFirewallPolicyManagedRuleOverride** létrehoz egy ruleOverride bejegyzést.</span><span class="sxs-lookup"><span data-stu-id="3e958-106">The **New-AzApplicationGatewayFirewallPolicyManagedRuleOverride** creates a ruleOverride entry.</span></span>

## <span data-ttu-id="3e958-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3e958-107">EXAMPLES</span></span>

### <span data-ttu-id="3e958-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3e958-108">Example 1</span></span>
```powershell
PS C:\> ruleOverrideEntry = New-AzApplicationGatewayFirewallPolicyManagedRuleOverride -RuleId $ruleId -State Disabled
```

<span data-ttu-id="3e958-109">Egy ruleOverride-bejegyzést hoz létre a RuleId-ban $ruleId és letiltva állapotként.</span><span class="sxs-lookup"><span data-stu-id="3e958-109">Creates a ruleOverride Entry with RuleId as $ruleId and State as Disabled.</span></span>

## <span data-ttu-id="3e958-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3e958-110">PARAMETERS</span></span>

### <span data-ttu-id="3e958-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e958-111">-DefaultProfile</span></span>
<span data-ttu-id="3e958-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3e958-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e958-113">-RuleId</span><span class="sxs-lookup"><span data-stu-id="3e958-113">-RuleId</span></span>
<span data-ttu-id="3e958-114">Adja meg a RuleId a szabály-bejegyzés felülbírálásához.</span><span class="sxs-lookup"><span data-stu-id="3e958-114">Specify the RuleId in override rule entry.</span></span>

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

### <span data-ttu-id="3e958-115">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="3e958-115">-State</span></span>
<span data-ttu-id="3e958-116">Adja meg a RuleId a szabály-bejegyzés felülbírálásához.</span><span class="sxs-lookup"><span data-stu-id="3e958-116">Specify the RuleId in override rule entry.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Disabled

Required: False
Position: Named
Default value: Disabled
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e958-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e958-117">CommonParameters</span></span>
<span data-ttu-id="3e958-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3e958-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e958-119">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3e958-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e958-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3e958-120">INPUTS</span></span>

### <span data-ttu-id="3e958-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="3e958-121">None</span></span>

## <span data-ttu-id="3e958-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3e958-122">OUTPUTS</span></span>

### <span data-ttu-id="3e958-123">Microsoft. Azure. commands. Network. models. PSApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="3e958-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>

## <span data-ttu-id="3e958-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3e958-124">NOTES</span></span>

## <span data-ttu-id="3e958-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3e958-125">RELATED LINKS</span></span>
