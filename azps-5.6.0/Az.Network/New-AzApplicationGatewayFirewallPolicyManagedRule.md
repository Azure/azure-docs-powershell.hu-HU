---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRule.md
ms.openlocfilehash: 73404a44ea26a07aad2869cc8fc94ef1c74ee987
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935658"
---
# <span data-ttu-id="7a39a-101">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="7a39a-101">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>

## <span data-ttu-id="7a39a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a39a-102">SYNOPSIS</span></span>
<span data-ttu-id="7a39a-103">Hozza létre a ManagedRules házirendet a tűzfal házirendhez.</span><span class="sxs-lookup"><span data-stu-id="7a39a-103">Create ManagedRules for the firewall policy.</span></span>

## <span data-ttu-id="7a39a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7a39a-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRule
 [-ManagedRuleSet <PSApplicationGatewayFirewallPolicyManagedRuleSet[]>]
 [-Exclusion <PSApplicationGatewayFirewallPolicyExclusion[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7a39a-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7a39a-105">DESCRIPTION</span></span>
<span data-ttu-id="7a39a-106">A **New-AzApplicationGatewayFirewallPolicyManagedRule** létrehoz egy felügyelt szabályokat egy tűzfalszabályhoz.</span><span class="sxs-lookup"><span data-stu-id="7a39a-106">The **New-AzApplicationGatewayFirewallPolicyManagedRule** creates a managed-rules for a firewall policy.</span></span>

## <span data-ttu-id="7a39a-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7a39a-107">EXAMPLES</span></span>

### <span data-ttu-id="7a39a-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="7a39a-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayFirewallPolicyManagedRule -ManagedRuleSet $managedRuleSet -Exclusion $exclusion1,$exclusion2
```

<span data-ttu-id="7a39a-109">A parancs létrehoz egy felügyelt szabálylistát a ManagedRuleSet listáról, $managedRuleSet egy kivétellistát pedig a következő bejegyzésekkel: $exclusion 1, $exclusion 2.</span><span class="sxs-lookup"><span data-stu-id="7a39a-109">The command creates managed rules a list of ManagedRuleSet with $managedRuleSet and an exclusion list with entries as $exclusion1, $exclusion2.</span></span>

## <span data-ttu-id="7a39a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7a39a-110">PARAMETERS</span></span>

### <span data-ttu-id="7a39a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a39a-111">-DefaultProfile</span></span>
<span data-ttu-id="7a39a-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7a39a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a39a-113">-Exclusion</span><span class="sxs-lookup"><span data-stu-id="7a39a-113">-Exclusion</span></span>
<span data-ttu-id="7a39a-114">Kivételbejegyzések listája.</span><span class="sxs-lookup"><span data-stu-id="7a39a-114">List of Exclusion Entry.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyExclusion[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a39a-115">-ManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="7a39a-115">-ManagedRuleSet</span></span>
<span data-ttu-id="7a39a-116">Felügyelt szabálykészletek listája.</span><span class="sxs-lookup"><span data-stu-id="7a39a-116">List of Managed ruleSets.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleSet[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a39a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a39a-117">CommonParameters</span></span>
<span data-ttu-id="7a39a-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a39a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a39a-119">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7a39a-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a39a-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7a39a-120">INPUTS</span></span>

### <span data-ttu-id="7a39a-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="7a39a-121">None</span></span>

## <span data-ttu-id="7a39a-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7a39a-122">OUTPUTS</span></span>

### <span data-ttu-id="7a39a-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRules</span><span class="sxs-lookup"><span data-stu-id="7a39a-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRules</span></span>

## <span data-ttu-id="7a39a-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7a39a-124">NOTES</span></span>

## <span data-ttu-id="7a39a-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7a39a-125">RELATED LINKS</span></span>
