---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfirewallcondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCondition.md
ms.openlocfilehash: 096fb182ae330750eeb23e365bc929edb17b21f4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007749"
---
# <span data-ttu-id="8ac4f-101">New-AzApplicationGatewayFirewallCondition</span><span class="sxs-lookup"><span data-stu-id="8ac4f-101">New-AzApplicationGatewayFirewallCondition</span></span>

## <span data-ttu-id="8ac4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ac4f-102">SYNOPSIS</span></span>
<span data-ttu-id="8ac4f-103">Egyezés feltételt hoz létre az egyéni szabályhoz</span><span class="sxs-lookup"><span data-stu-id="8ac4f-103">Creates a match condition for custom rule</span></span>

## <span data-ttu-id="8ac4f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8ac4f-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallCondition -MatchVariable <PSApplicationGatewayFirewallMatchVariable[]>
 -Operator <String> [-NegationCondition <Boolean>] -MatchValue <String[]> [-Transform <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ac4f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8ac4f-105">DESCRIPTION</span></span>
<span data-ttu-id="8ac4f-106">A **New-AzApplicationGatewayFirewallCondition** létrehoz egyezés feltételt az egyéni tűzfalszabályhoz.</span><span class="sxs-lookup"><span data-stu-id="8ac4f-106">The **New-AzApplicationGatewayFirewallCondition** creates a match condition for firewall custom rule.</span></span>

## <span data-ttu-id="8ac4f-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8ac4f-107">EXAMPLES</span></span>

### <span data-ttu-id="8ac4f-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="8ac4f-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayFirewallCondition -MatchVariable $variable -Operator Contains -NegationCondition false -Transforms Lowercase, Trim -MatchValue abc, cde
```

<span data-ttu-id="8ac4f-109">A parancs új egyezést hoz létre a $variable-ben definiált egyezésváltozós változóval, az operátor Tartalmazza és a negation feltétel hamis, a Transzfroms (beleértve a kisbetűket és a vágást is) és az egyezés értéke abc és cde.</span><span class="sxs-lookup"><span data-stu-id="8ac4f-109">The command creates a new match condition using the match variable defined in the $variable, the operator is Contains and negation condition is false, Transfroms including lowercase and trim, the match value is abc and cde.</span></span> <span data-ttu-id="8ac4f-110">Az új egyezés feltételt a rendszer a $condition.</span><span class="sxs-lookup"><span data-stu-id="8ac4f-110">The new match condition is saved in $condition.</span></span>

## <span data-ttu-id="8ac4f-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8ac4f-111">PARAMETERS</span></span>

### <span data-ttu-id="8ac4f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ac4f-112">-DefaultProfile</span></span>
<span data-ttu-id="8ac4f-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8ac4f-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ac4f-114">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="8ac4f-114">-MatchValue</span></span>
<span data-ttu-id="8ac4f-115">Érték egyeztetése</span><span class="sxs-lookup"><span data-stu-id="8ac4f-115">Match value.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ac4f-116">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="8ac4f-116">-MatchVariable</span></span>
<span data-ttu-id="8ac4f-117">Egyezés változók listája.</span><span class="sxs-lookup"><span data-stu-id="8ac4f-117">List of match variables.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallMatchVariable[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ac4f-118">-NegationCondition</span><span class="sxs-lookup"><span data-stu-id="8ac4f-118">-NegationCondition</span></span>
<span data-ttu-id="8ac4f-119">Azt írja le, hogy ez nem egy feltétel-e.</span><span class="sxs-lookup"><span data-stu-id="8ac4f-119">Describes if this is negate condition or not.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ac4f-120">-Operátor</span><span class="sxs-lookup"><span data-stu-id="8ac4f-120">-Operator</span></span>
<span data-ttu-id="8ac4f-121">Az egyező operátort ismerteti.</span><span class="sxs-lookup"><span data-stu-id="8ac4f-121">Describes operator to be matched.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPMatch, Equal, Contains, LessThan, GreaterThan, LessThanOrEqual, GreaterThanOrEqual, BeginsWith, EndsWith, Regex

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ac4f-122">-Átalakítás</span><span class="sxs-lookup"><span data-stu-id="8ac4f-122">-Transform</span></span>
<span data-ttu-id="8ac4f-123">Átalakítások listája.</span><span class="sxs-lookup"><span data-stu-id="8ac4f-123">List of transforms.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Lowercase, Trim, UrlDecode, UrlEncode, RemoveNulls, HtmlEntityDecode

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ac4f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ac4f-124">CommonParameters</span></span>
<span data-ttu-id="8ac4f-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ac4f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ac4f-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ac4f-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ac4f-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8ac4f-127">INPUTS</span></span>

### <span data-ttu-id="8ac4f-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="8ac4f-128">None</span></span>

## <span data-ttu-id="8ac4f-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8ac4f-129">OUTPUTS</span></span>

### <span data-ttu-id="8ac4f-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCondition</span><span class="sxs-lookup"><span data-stu-id="8ac4f-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCondition</span></span>

## <span data-ttu-id="8ac4f-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8ac4f-131">NOTES</span></span>

## <span data-ttu-id="8ac4f-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8ac4f-132">RELATED LINKS</span></span>
