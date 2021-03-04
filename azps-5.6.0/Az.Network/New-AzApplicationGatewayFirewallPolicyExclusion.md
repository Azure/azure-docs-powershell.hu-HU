---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfirewallpolicyexclusion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyExclusion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyExclusion.md
ms.openlocfilehash: 04cf39f9c0d8774ffb02688e4edf5804029df669
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930010"
---
# <span data-ttu-id="d1dd1-101">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="d1dd1-101">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>

## <span data-ttu-id="d1dd1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1dd1-102">SYNOPSIS</span></span>
<span data-ttu-id="d1dd1-103">Kivételt hoz létre a tűzfal házirendjében</span><span class="sxs-lookup"><span data-stu-id="d1dd1-103">Creates an exclusion on the Firewall Policy</span></span>

## <span data-ttu-id="d1dd1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d1dd1-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyExclusion -MatchVariable <String> -SelectorMatchOperator <String>
 -Selector <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1dd1-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d1dd1-105">DESCRIPTION</span></span>
<span data-ttu-id="d1dd1-106">The **New-AzApplicationGatewayFirewallPolicyExclusion** cmdlet a new exclusion rule list for firewall policy.</span><span class="sxs-lookup"><span data-stu-id="d1dd1-106">The **New-AzApplicationGatewayFirewallPolicyExclusion** cmdlet a new exclusion rule list for firewall policy.</span></span>

## <span data-ttu-id="d1dd1-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d1dd1-107">EXAMPLES</span></span>

### <span data-ttu-id="d1dd1-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="d1dd1-108">Example 1</span></span>
```powershell
PS C:\> $exclusionEntry = New-AzApplicationGatewayFirewallPolicyExclusion -MatchVariable "RequestHeaderNames" -SelectorMatchOperator "StartsWith" -Selector "xyz"
```

<span data-ttu-id="d1dd1-109">Ez a parancs új kivételbejegyzést hoz létre a RequestHeaderNames nevű változóhoz és az xyz nevű StartsWith és Selector operátorhoz.</span><span class="sxs-lookup"><span data-stu-id="d1dd1-109">This command creates a new exclusion-entry for the variable named RequestHeaderNames and operator named StartsWith and Selector named xyz.</span></span> <span data-ttu-id="d1dd1-110">A kivételbejegyzést a rendszer a $exclusionEntry.</span><span class="sxs-lookup"><span data-stu-id="d1dd1-110">The exclusion entry is saved in $exclusionEntry.</span></span>

## <span data-ttu-id="d1dd1-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d1dd1-111">PARAMETERS</span></span>

### <span data-ttu-id="d1dd1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1dd1-112">-DefaultProfile</span></span>
<span data-ttu-id="d1dd1-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d1dd1-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1dd1-114">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="d1dd1-114">-MatchVariable</span></span>
<span data-ttu-id="d1dd1-115">Az a változó, amelyből ki kell zárni.</span><span class="sxs-lookup"><span data-stu-id="d1dd1-115">The variable to be excluded.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RequestHeaderNames, RequestCookieNames, RequestArgNames

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1dd1-116">-Választó</span><span class="sxs-lookup"><span data-stu-id="d1dd1-116">-Selector</span></span>
<span data-ttu-id="d1dd1-117">Ha a változó egy gyűjtemény, az operátor azt határozza meg, hogy a gyűjtemény mely elemeire vonatkozik ez a kivétel.</span><span class="sxs-lookup"><span data-stu-id="d1dd1-117">When variable is a collection, operator used to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="d1dd1-118">-SelectorMatchOperator</span><span class="sxs-lookup"><span data-stu-id="d1dd1-118">-SelectorMatchOperator</span></span>
<span data-ttu-id="d1dd1-119">Ha a változó egy gyűjtemény, a választóval megadhatja, hogy a gyűjtemény mely elemeire vonatkozik ez a kivétel.</span><span class="sxs-lookup"><span data-stu-id="d1dd1-119">When variable is a collection, operate on the selector to specify which elements in the collection this exclusion applies to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Equals, Contains, StartsWith, EndsWith, EqualsAny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1dd1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1dd1-120">CommonParameters</span></span>
<span data-ttu-id="d1dd1-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1dd1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1dd1-122">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d1dd1-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1dd1-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d1dd1-123">INPUTS</span></span>

### <span data-ttu-id="d1dd1-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="d1dd1-124">None</span></span>

## <span data-ttu-id="d1dd1-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d1dd1-125">OUTPUTS</span></span>

### <span data-ttu-id="d1dd1-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="d1dd1-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyExclusion</span></span>

## <span data-ttu-id="d1dd1-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d1dd1-127">NOTES</span></span>

## <span data-ttu-id="d1dd1-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d1dd1-128">RELATED LINKS</span></span>
