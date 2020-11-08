---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallcondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCondition.md
ms.openlocfilehash: 64157cd137e9f3b784404dccee6513b6fe023d0f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195662"
---
# <span data-ttu-id="0f0d4-101">New-AzApplicationGatewayFirewallCondition</span><span class="sxs-lookup"><span data-stu-id="0f0d4-101">New-AzApplicationGatewayFirewallCondition</span></span>

## <span data-ttu-id="0f0d4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0f0d4-102">SYNOPSIS</span></span>
<span data-ttu-id="0f0d4-103">Egyeztető feltételt hoz létre az egyéni szabályokhoz.</span><span class="sxs-lookup"><span data-stu-id="0f0d4-103">Creates a match condition for custom rule</span></span>

## <span data-ttu-id="0f0d4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0f0d4-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallCondition -MatchVariable <PSApplicationGatewayFirewallMatchVariable[]>
 -Operator <String> [-NegationCondition <Boolean>] -MatchValue <String[]> [-Transform <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f0d4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0f0d4-105">DESCRIPTION</span></span>
<span data-ttu-id="0f0d4-106">A **New-AzApplicationGatewayFirewallCondition** létrehoz egy egyeztetési feltételt a tűzfal egyéni szabályához.</span><span class="sxs-lookup"><span data-stu-id="0f0d4-106">The **New-AzApplicationGatewayFirewallCondition** creates a match condition for firewall custom rule.</span></span>

## <span data-ttu-id="0f0d4-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0f0d4-107">EXAMPLES</span></span>

### <span data-ttu-id="0f0d4-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="0f0d4-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayFirewallCondition -MatchVariable $variable -Operator Contains -NegationCondition false -Transforms Lowercase, Trim -MatchValue abc, cde
```

<span data-ttu-id="0f0d4-109">A parancs új egyeztetési feltételt hoz létre a $variableban definiált egyezési változóval, az operátor tartalmaz és tagadási feltételt tartalmaz, a Transfroms, például a kisbetűs és a kimetszet, a hol. van érték az ABC és a CDE.</span><span class="sxs-lookup"><span data-stu-id="0f0d4-109">The command creates a new match condition using the match variable defined in the $variable, the operator is Contains and negation condition is false, Transfroms including lowercase and trim, the match value is abc and cde.</span></span> <span data-ttu-id="0f0d4-110">A program az új egyezési feltételt $condition menti.</span><span class="sxs-lookup"><span data-stu-id="0f0d4-110">The new match condition is saved in $condition.</span></span>

## <span data-ttu-id="0f0d4-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0f0d4-111">PARAMETERS</span></span>

### <span data-ttu-id="0f0d4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f0d4-112">-DefaultProfile</span></span>
<span data-ttu-id="0f0d4-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0f0d4-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f0d4-114">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="0f0d4-114">-MatchValue</span></span>
<span data-ttu-id="0f0d4-115">Az érték egyeztetése</span><span class="sxs-lookup"><span data-stu-id="0f0d4-115">Match value.</span></span>

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

### <span data-ttu-id="0f0d4-116">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="0f0d4-116">-MatchVariable</span></span>
<span data-ttu-id="0f0d4-117">A egyezési változók listája.</span><span class="sxs-lookup"><span data-stu-id="0f0d4-117">List of match variables.</span></span>

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

### <span data-ttu-id="0f0d4-118">-NegationCondition</span><span class="sxs-lookup"><span data-stu-id="0f0d4-118">-NegationCondition</span></span>
<span data-ttu-id="0f0d4-119">Ez a cikk azt ismerteti, hogy a feltétel nincs-e megtagadva.</span><span class="sxs-lookup"><span data-stu-id="0f0d4-119">Describes if this is negate condition or not.</span></span>

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

### <span data-ttu-id="0f0d4-120">-Operátor</span><span class="sxs-lookup"><span data-stu-id="0f0d4-120">-Operator</span></span>
<span data-ttu-id="0f0d4-121">A megfelelő operátort ismerteti.</span><span class="sxs-lookup"><span data-stu-id="0f0d4-121">Describes operator to be matched.</span></span>

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

### <span data-ttu-id="0f0d4-122">-Transform</span><span class="sxs-lookup"><span data-stu-id="0f0d4-122">-Transform</span></span>
<span data-ttu-id="0f0d4-123">Az átalakítások listája.</span><span class="sxs-lookup"><span data-stu-id="0f0d4-123">List of transforms.</span></span>

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

### <span data-ttu-id="0f0d4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f0d4-124">CommonParameters</span></span>
<span data-ttu-id="0f0d4-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0f0d4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f0d4-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f0d4-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f0d4-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0f0d4-127">INPUTS</span></span>

### <span data-ttu-id="0f0d4-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="0f0d4-128">None</span></span>

## <span data-ttu-id="0f0d4-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0f0d4-129">OUTPUTS</span></span>

### <span data-ttu-id="0f0d4-130">Microsoft. Azure. commands. Network. models. PSApplicationGatewayFirewallCondition</span><span class="sxs-lookup"><span data-stu-id="0f0d4-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCondition</span></span>

## <span data-ttu-id="0f0d4-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0f0d4-131">NOTES</span></span>

## <span data-ttu-id="0f0d4-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0f0d4-132">RELATED LINKS</span></span>
