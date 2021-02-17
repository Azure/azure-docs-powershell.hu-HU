---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallcondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCondition.md
ms.openlocfilehash: 64157cd137e9f3b784404dccee6513b6fe023d0f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147027"
---
# <span data-ttu-id="d558e-101">New-AzApplicationGatewayFirewallCondition</span><span class="sxs-lookup"><span data-stu-id="d558e-101">New-AzApplicationGatewayFirewallCondition</span></span>

## <span data-ttu-id="d558e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d558e-102">SYNOPSIS</span></span>
<span data-ttu-id="d558e-103">Egyezés feltételt hoz létre az egyéni szabályhoz</span><span class="sxs-lookup"><span data-stu-id="d558e-103">Creates a match condition for custom rule</span></span>

## <span data-ttu-id="d558e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d558e-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallCondition -MatchVariable <PSApplicationGatewayFirewallMatchVariable[]>
 -Operator <String> [-NegationCondition <Boolean>] -MatchValue <String[]> [-Transform <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d558e-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d558e-105">DESCRIPTION</span></span>
<span data-ttu-id="d558e-106">A **New-AzApplicationGatewayFirewallCondition** létrehoz egyezés feltételt az egyéni tűzfalszabályhoz.</span><span class="sxs-lookup"><span data-stu-id="d558e-106">The **New-AzApplicationGatewayFirewallCondition** creates a match condition for firewall custom rule.</span></span>

## <span data-ttu-id="d558e-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d558e-107">EXAMPLES</span></span>

### <span data-ttu-id="d558e-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="d558e-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayFirewallCondition -MatchVariable $variable -Operator Contains -NegationCondition false -Transforms Lowercase, Trim -MatchValue abc, cde
```

<span data-ttu-id="d558e-109">A parancs új egyezés feltételt hoz létre a $variable-ben definiált egyezésváltozóval, az operátor Tartalmazza és a negation feltétel hamis, a Transzfroms (beleértve a kisbetűket és a vágást is) és az egyezés értéke abc és cde.</span><span class="sxs-lookup"><span data-stu-id="d558e-109">The command creates a new match condition using the match variable defined in the $variable, the operator is Contains and negation condition is false, Transfroms including lowercase and trim, the match value is abc and cde.</span></span> <span data-ttu-id="d558e-110">Az új egyezés feltételt a rendszer a $condition.</span><span class="sxs-lookup"><span data-stu-id="d558e-110">The new match condition is saved in $condition.</span></span>

## <span data-ttu-id="d558e-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d558e-111">PARAMETERS</span></span>

### <span data-ttu-id="d558e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d558e-112">-DefaultProfile</span></span>
<span data-ttu-id="d558e-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d558e-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d558e-114">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="d558e-114">-MatchValue</span></span>
<span data-ttu-id="d558e-115">Érték egyeztetése</span><span class="sxs-lookup"><span data-stu-id="d558e-115">Match value.</span></span>

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

### <span data-ttu-id="d558e-116">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="d558e-116">-MatchVariable</span></span>
<span data-ttu-id="d558e-117">Egyezés változók listája.</span><span class="sxs-lookup"><span data-stu-id="d558e-117">List of match variables.</span></span>

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

### <span data-ttu-id="d558e-118">-NegationCondition</span><span class="sxs-lookup"><span data-stu-id="d558e-118">-NegationCondition</span></span>
<span data-ttu-id="d558e-119">Azt írja le, hogy ez nem egy feltétel-e.</span><span class="sxs-lookup"><span data-stu-id="d558e-119">Describes if this is negate condition or not.</span></span>

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

### <span data-ttu-id="d558e-120">-Operátor</span><span class="sxs-lookup"><span data-stu-id="d558e-120">-Operator</span></span>
<span data-ttu-id="d558e-121">Az egyező operátort ismerteti.</span><span class="sxs-lookup"><span data-stu-id="d558e-121">Describes operator to be matched.</span></span>

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

### <span data-ttu-id="d558e-122">-Átalakítás</span><span class="sxs-lookup"><span data-stu-id="d558e-122">-Transform</span></span>
<span data-ttu-id="d558e-123">Átalakítások listája.</span><span class="sxs-lookup"><span data-stu-id="d558e-123">List of transforms.</span></span>

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

### <span data-ttu-id="d558e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d558e-124">CommonParameters</span></span>
<span data-ttu-id="d558e-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d558e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d558e-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d558e-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d558e-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d558e-127">INPUTS</span></span>

### <span data-ttu-id="d558e-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="d558e-128">None</span></span>

## <span data-ttu-id="d558e-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d558e-129">OUTPUTS</span></span>

### <span data-ttu-id="d558e-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCondition</span><span class="sxs-lookup"><span data-stu-id="d558e-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCondition</span></span>

## <span data-ttu-id="d558e-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d558e-131">NOTES</span></span>

## <span data-ttu-id="d558e-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d558e-132">RELATED LINKS</span></span>
