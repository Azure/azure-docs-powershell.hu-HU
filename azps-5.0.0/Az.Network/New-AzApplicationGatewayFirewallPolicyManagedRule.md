---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRule.md
ms.openlocfilehash: 6b709283024a37d85bfac89f7e2fec4448544729
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185257"
---
# <span data-ttu-id="d2ef2-101">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="d2ef2-101">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>

## <span data-ttu-id="d2ef2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d2ef2-102">SYNOPSIS</span></span>
<span data-ttu-id="d2ef2-103">ManagedRules létrehozása a tűzfal házirendjéhez</span><span class="sxs-lookup"><span data-stu-id="d2ef2-103">Create ManagedRules for the firewall policy.</span></span>

## <span data-ttu-id="d2ef2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d2ef2-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRule
 [-ManagedRuleSet <PSApplicationGatewayFirewallPolicyManagedRuleSet[]>]
 [-Exclusion <PSApplicationGatewayFirewallPolicyExclusion[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d2ef2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d2ef2-105">DESCRIPTION</span></span>
<span data-ttu-id="d2ef2-106">A **New-AzApplicationGatewayFirewallPolicyManagedRule** létrehoz egy felügyelt szabályokat a tűzfal házirendjéhez.</span><span class="sxs-lookup"><span data-stu-id="d2ef2-106">The **New-AzApplicationGatewayFirewallPolicyManagedRule** creates a managed-rules for a firewall policy.</span></span>

## <span data-ttu-id="d2ef2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d2ef2-107">EXAMPLES</span></span>

### <span data-ttu-id="d2ef2-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d2ef2-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayFirewallPolicyManagedRule -ManagedRuleSet $managedRuleSet -Exclusion $exclusion1,$exclusion2
```

<span data-ttu-id="d2ef2-109">A parancs felügyelt szabályokat hoz létre a ManagedRuleSet-val $managedRuleSet és egy, a $exclusion 1, $exclusion 2 bejegyzést tartalmazó listával.</span><span class="sxs-lookup"><span data-stu-id="d2ef2-109">The command creates managed rules a list of ManagedRuleSet with $managedRuleSet and an exclusion list with entries as $exclusion1, $exclusion2.</span></span>

## <span data-ttu-id="d2ef2-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d2ef2-110">PARAMETERS</span></span>

### <span data-ttu-id="d2ef2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2ef2-111">-DefaultProfile</span></span>
<span data-ttu-id="d2ef2-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d2ef2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2ef2-113">– Kizárás</span><span class="sxs-lookup"><span data-stu-id="d2ef2-113">-Exclusion</span></span>
<span data-ttu-id="d2ef2-114">A kizárási bejegyzés listája</span><span class="sxs-lookup"><span data-stu-id="d2ef2-114">List of Exclusion Entry.</span></span>

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

### <span data-ttu-id="d2ef2-115">-ManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="d2ef2-115">-ManagedRuleSet</span></span>
<span data-ttu-id="d2ef2-116">A felügyelt szabályrendszerek listája.</span><span class="sxs-lookup"><span data-stu-id="d2ef2-116">List of Managed ruleSets.</span></span>

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

### <span data-ttu-id="d2ef2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2ef2-117">CommonParameters</span></span>
<span data-ttu-id="d2ef2-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d2ef2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2ef2-119">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d2ef2-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2ef2-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d2ef2-120">INPUTS</span></span>

### <span data-ttu-id="d2ef2-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="d2ef2-121">None</span></span>

## <span data-ttu-id="d2ef2-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d2ef2-122">OUTPUTS</span></span>

### <span data-ttu-id="d2ef2-123">Microsoft. Azure. commands. Network. models. PSApplicationGatewayFirewallPolicyManagedRules</span><span class="sxs-lookup"><span data-stu-id="d2ef2-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRules</span></span>

## <span data-ttu-id="d2ef2-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d2ef2-124">NOTES</span></span>

## <span data-ttu-id="d2ef2-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d2ef2-125">RELATED LINKS</span></span>
