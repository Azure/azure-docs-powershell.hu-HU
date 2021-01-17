---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRule.md
ms.openlocfilehash: 6b709283024a37d85bfac89f7e2fec4448544729
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467338"
---
# <span data-ttu-id="bce86-101">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="bce86-101">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>

## <span data-ttu-id="bce86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bce86-102">SYNOPSIS</span></span>
<span data-ttu-id="bce86-103">Hozza létre a ManagedRules tartományt a tűzfal házirendhez.</span><span class="sxs-lookup"><span data-stu-id="bce86-103">Create ManagedRules for the firewall policy.</span></span>

## <span data-ttu-id="bce86-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bce86-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRule
 [-ManagedRuleSet <PSApplicationGatewayFirewallPolicyManagedRuleSet[]>]
 [-Exclusion <PSApplicationGatewayFirewallPolicyExclusion[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bce86-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bce86-105">DESCRIPTION</span></span>
<span data-ttu-id="bce86-106">A **New-AzApplicationGatewayFirewallPolicyManagedRule** létrehoz egy felügyelt szabályokat egy tűzfalszabályhoz.</span><span class="sxs-lookup"><span data-stu-id="bce86-106">The **New-AzApplicationGatewayFirewallPolicyManagedRule** creates a managed-rules for a firewall policy.</span></span>

## <span data-ttu-id="bce86-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bce86-107">EXAMPLES</span></span>

### <span data-ttu-id="bce86-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="bce86-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayFirewallPolicyManagedRule -ManagedRuleSet $managedRuleSet -Exclusion $exclusion1,$exclusion2
```

<span data-ttu-id="bce86-109">A parancs létrehoz egy felügyelt szabálylistát a ManagedRuleSet listáról, $managedRuleSet egy kivétellistát pedig a következő bejegyzésekkel: $exclusion 1, $exclusion 2.</span><span class="sxs-lookup"><span data-stu-id="bce86-109">The command creates managed rules a list of ManagedRuleSet with $managedRuleSet and an exclusion list with entries as $exclusion1, $exclusion2.</span></span>

## <span data-ttu-id="bce86-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bce86-110">PARAMETERS</span></span>

### <span data-ttu-id="bce86-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bce86-111">-DefaultProfile</span></span>
<span data-ttu-id="bce86-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bce86-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bce86-113">-Exclusion</span><span class="sxs-lookup"><span data-stu-id="bce86-113">-Exclusion</span></span>
<span data-ttu-id="bce86-114">Kivételbejegyzések listája.</span><span class="sxs-lookup"><span data-stu-id="bce86-114">List of Exclusion Entry.</span></span>

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

### <span data-ttu-id="bce86-115">-ManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="bce86-115">-ManagedRuleSet</span></span>
<span data-ttu-id="bce86-116">Felügyelt szabálykészletek listája.</span><span class="sxs-lookup"><span data-stu-id="bce86-116">List of Managed ruleSets.</span></span>

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

### <span data-ttu-id="bce86-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bce86-117">CommonParameters</span></span>
<span data-ttu-id="bce86-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bce86-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bce86-119">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bce86-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bce86-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bce86-120">INPUTS</span></span>

### <span data-ttu-id="bce86-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="bce86-121">None</span></span>

## <span data-ttu-id="bce86-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bce86-122">OUTPUTS</span></span>

### <span data-ttu-id="bce86-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRules</span><span class="sxs-lookup"><span data-stu-id="bce86-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRules</span></span>

## <span data-ttu-id="bce86-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bce86-124">NOTES</span></span>

## <span data-ttu-id="bce86-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bce86-125">RELATED LINKS</span></span>
