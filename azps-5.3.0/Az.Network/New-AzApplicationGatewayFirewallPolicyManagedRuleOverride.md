---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedruleoverride
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleOverride.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleOverride.md
ms.openlocfilehash: a3e057b8fbf6b04f48936b2aa96e9696964e5061
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385614"
---
# <span data-ttu-id="81a24-101">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="81a24-101">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>

## <span data-ttu-id="81a24-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81a24-102">SYNOPSIS</span></span>
<span data-ttu-id="81a24-103">FelügyeltRuleOverride-bejegyzést hoz létre a RuleGroupOverrideGroup bejegyzéshez.</span><span class="sxs-lookup"><span data-stu-id="81a24-103">Creates a managedRuleOverride entry for RuleGroupOverrideGroup entry.</span></span>

## <span data-ttu-id="81a24-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="81a24-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRuleOverride -RuleId <String> [-State <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81a24-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="81a24-105">DESCRIPTION</span></span>
<span data-ttu-id="81a24-106">A **New-AzApplicationGatewayFirewallPolicyManagedRuleOverride** létrehoz egy ruleOverride bejegyzést.</span><span class="sxs-lookup"><span data-stu-id="81a24-106">The **New-AzApplicationGatewayFirewallPolicyManagedRuleOverride** creates a ruleOverride entry.</span></span>

## <span data-ttu-id="81a24-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="81a24-107">EXAMPLES</span></span>

### <span data-ttu-id="81a24-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="81a24-108">Example 1</span></span>
```powershell
PS C:\> ruleOverrideEntry = New-AzApplicationGatewayFirewallPolicyManagedRuleOverride -RuleId $ruleId -State Disabled
```

<span data-ttu-id="81a24-109">Létrehoz egy ruleOverride entry with RuleId as $ruleId state as Disabled.</span><span class="sxs-lookup"><span data-stu-id="81a24-109">Creates a ruleOverride Entry with RuleId as $ruleId and State as Disabled.</span></span>

## <span data-ttu-id="81a24-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="81a24-110">PARAMETERS</span></span>

### <span data-ttu-id="81a24-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81a24-111">-DefaultProfile</span></span>
<span data-ttu-id="81a24-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="81a24-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81a24-113">-RuleId</span><span class="sxs-lookup"><span data-stu-id="81a24-113">-RuleId</span></span>
<span data-ttu-id="81a24-114">Adja meg a Szabályazonosítót a szabály felülbírálása bejegyzésben.</span><span class="sxs-lookup"><span data-stu-id="81a24-114">Specify the RuleId in override rule entry.</span></span>

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

### <span data-ttu-id="81a24-115">-State</span><span class="sxs-lookup"><span data-stu-id="81a24-115">-State</span></span>
<span data-ttu-id="81a24-116">Adja meg a Szabályazonosítót a szabály felülbírálása bejegyzésben.</span><span class="sxs-lookup"><span data-stu-id="81a24-116">Specify the RuleId in override rule entry.</span></span>

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

### <span data-ttu-id="81a24-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81a24-117">CommonParameters</span></span>
<span data-ttu-id="81a24-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81a24-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81a24-119">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="81a24-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81a24-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="81a24-120">INPUTS</span></span>

### <span data-ttu-id="81a24-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="81a24-121">None</span></span>

## <span data-ttu-id="81a24-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="81a24-122">OUTPUTS</span></span>

### <span data-ttu-id="81a24-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="81a24-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>

## <span data-ttu-id="81a24-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="81a24-124">NOTES</span></span>

## <span data-ttu-id="81a24-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="81a24-125">RELATED LINKS</span></span>
