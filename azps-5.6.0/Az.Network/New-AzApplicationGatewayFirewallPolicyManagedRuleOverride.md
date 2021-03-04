---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedruleoverride
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleOverride.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleOverride.md
ms.openlocfilehash: 31c12fd53c8aa6c886ab5e26a8c35996045335e4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939529"
---
# <span data-ttu-id="01e5c-101">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="01e5c-101">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>

## <span data-ttu-id="01e5c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01e5c-102">SYNOPSIS</span></span>
<span data-ttu-id="01e5c-103">FelügyeltRuleOverride-bejegyzést hoz létre a RuleGroupOverrideGroup bejegyzéshez.</span><span class="sxs-lookup"><span data-stu-id="01e5c-103">Creates a managedRuleOverride entry for RuleGroupOverrideGroup entry.</span></span>

## <span data-ttu-id="01e5c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="01e5c-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRuleOverride -RuleId <String> [-State <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01e5c-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="01e5c-105">DESCRIPTION</span></span>
<span data-ttu-id="01e5c-106">A **New-AzApplicationGatewayFirewallPolicyManagedRuleOverride** létrehoz egy ruleOverride bejegyzést.</span><span class="sxs-lookup"><span data-stu-id="01e5c-106">The **New-AzApplicationGatewayFirewallPolicyManagedRuleOverride** creates a ruleOverride entry.</span></span>

## <span data-ttu-id="01e5c-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="01e5c-107">EXAMPLES</span></span>

### <span data-ttu-id="01e5c-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="01e5c-108">Example 1</span></span>
```powershell
PS C:\> ruleOverrideEntry = New-AzApplicationGatewayFirewallPolicyManagedRuleOverride -RuleId $ruleId -State Disabled
```

<span data-ttu-id="01e5c-109">Létrehoz egy ruleOverride entry with RuleId as $ruleId state as Disabled.</span><span class="sxs-lookup"><span data-stu-id="01e5c-109">Creates a ruleOverride Entry with RuleId as $ruleId and State as Disabled.</span></span>

## <span data-ttu-id="01e5c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="01e5c-110">PARAMETERS</span></span>

### <span data-ttu-id="01e5c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01e5c-111">-DefaultProfile</span></span>
<span data-ttu-id="01e5c-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="01e5c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01e5c-113">-RuleId</span><span class="sxs-lookup"><span data-stu-id="01e5c-113">-RuleId</span></span>
<span data-ttu-id="01e5c-114">Adja meg a Szabályazonosítót a szabály felülbírálása bejegyzésben.</span><span class="sxs-lookup"><span data-stu-id="01e5c-114">Specify the RuleId in override rule entry.</span></span>

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

### <span data-ttu-id="01e5c-115">-State</span><span class="sxs-lookup"><span data-stu-id="01e5c-115">-State</span></span>
<span data-ttu-id="01e5c-116">Adja meg a Szabályazonosítót a szabály felülbírálása bejegyzésben.</span><span class="sxs-lookup"><span data-stu-id="01e5c-116">Specify the RuleId in override rule entry.</span></span>

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

### <span data-ttu-id="01e5c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01e5c-117">CommonParameters</span></span>
<span data-ttu-id="01e5c-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01e5c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01e5c-119">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="01e5c-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01e5c-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="01e5c-120">INPUTS</span></span>

### <span data-ttu-id="01e5c-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="01e5c-121">None</span></span>

## <span data-ttu-id="01e5c-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="01e5c-122">OUTPUTS</span></span>

### <span data-ttu-id="01e5c-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="01e5c-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>

## <span data-ttu-id="01e5c-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="01e5c-124">NOTES</span></span>

## <span data-ttu-id="01e5c-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="01e5c-125">RELATED LINKS</span></span>
