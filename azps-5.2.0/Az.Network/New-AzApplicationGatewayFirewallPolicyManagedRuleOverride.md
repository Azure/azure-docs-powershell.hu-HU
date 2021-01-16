---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedruleoverride
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleOverride.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleOverride.md
ms.openlocfilehash: a3e057b8fbf6b04f48936b2aa96e9696964e5061
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98340230"
---
# <span data-ttu-id="f6c7a-101">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="f6c7a-101">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>

## <span data-ttu-id="f6c7a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6c7a-102">SYNOPSIS</span></span>
<span data-ttu-id="f6c7a-103">FelügyeltRuleOverride-bejegyzést hoz létre a RuleGroupOverrideGroup bejegyzéshez.</span><span class="sxs-lookup"><span data-stu-id="f6c7a-103">Creates a managedRuleOverride entry for RuleGroupOverrideGroup entry.</span></span>

## <span data-ttu-id="f6c7a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f6c7a-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRuleOverride -RuleId <String> [-State <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6c7a-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f6c7a-105">DESCRIPTION</span></span>
<span data-ttu-id="f6c7a-106">A **New-AzApplicationGatewayFirewallPolicyManagedRuleOverride** létrehoz egy ruleOverride bejegyzést.</span><span class="sxs-lookup"><span data-stu-id="f6c7a-106">The **New-AzApplicationGatewayFirewallPolicyManagedRuleOverride** creates a ruleOverride entry.</span></span>

## <span data-ttu-id="f6c7a-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f6c7a-107">EXAMPLES</span></span>

### <span data-ttu-id="f6c7a-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="f6c7a-108">Example 1</span></span>
```powershell
PS C:\> ruleOverrideEntry = New-AzApplicationGatewayFirewallPolicyManagedRuleOverride -RuleId $ruleId -State Disabled
```

<span data-ttu-id="f6c7a-109">Létrehoz egy ruleOverride entry with RuleId as $ruleId state as Disabled.</span><span class="sxs-lookup"><span data-stu-id="f6c7a-109">Creates a ruleOverride Entry with RuleId as $ruleId and State as Disabled.</span></span>

## <span data-ttu-id="f6c7a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f6c7a-110">PARAMETERS</span></span>

### <span data-ttu-id="f6c7a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6c7a-111">-DefaultProfile</span></span>
<span data-ttu-id="f6c7a-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f6c7a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6c7a-113">-RuleId</span><span class="sxs-lookup"><span data-stu-id="f6c7a-113">-RuleId</span></span>
<span data-ttu-id="f6c7a-114">Adja meg a Szabályazonosítót a szabály felülbírálása bejegyzésben.</span><span class="sxs-lookup"><span data-stu-id="f6c7a-114">Specify the RuleId in override rule entry.</span></span>

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

### <span data-ttu-id="f6c7a-115">-State</span><span class="sxs-lookup"><span data-stu-id="f6c7a-115">-State</span></span>
<span data-ttu-id="f6c7a-116">Adja meg a Szabályazonosítót a szabály felülbírálása bejegyzésben.</span><span class="sxs-lookup"><span data-stu-id="f6c7a-116">Specify the RuleId in override rule entry.</span></span>

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

### <span data-ttu-id="f6c7a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6c7a-117">CommonParameters</span></span>
<span data-ttu-id="f6c7a-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6c7a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6c7a-119">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f6c7a-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6c7a-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f6c7a-120">INPUTS</span></span>

### <span data-ttu-id="f6c7a-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="f6c7a-121">None</span></span>

## <span data-ttu-id="f6c7a-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f6c7a-122">OUTPUTS</span></span>

### <span data-ttu-id="f6c7a-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="f6c7a-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>

## <span data-ttu-id="f6c7a-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f6c7a-124">NOTES</span></span>

## <span data-ttu-id="f6c7a-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f6c7a-125">RELATED LINKS</span></span>
