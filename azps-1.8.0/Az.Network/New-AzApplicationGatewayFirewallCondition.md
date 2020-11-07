---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallcondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCondition.md
ms.openlocfilehash: ee7f6f2b824041cf56b27c34dc70358c4229e527
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670424"
---
# <span data-ttu-id="e403a-101">New-AzApplicationGatewayFirewallCondition</span><span class="sxs-lookup"><span data-stu-id="e403a-101">New-AzApplicationGatewayFirewallCondition</span></span>

## <span data-ttu-id="e403a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e403a-102">SYNOPSIS</span></span>
<span data-ttu-id="e403a-103">Egyeztető feltételt hoz létre az egyéni szabályokhoz.</span><span class="sxs-lookup"><span data-stu-id="e403a-103">Creates a match condition for custom rule</span></span>

## <span data-ttu-id="e403a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e403a-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallCondition -MatchVariable <PSApplicationGatewayFirewallMatchVariable[]>
 -Operator <String> [-NegationCondition <Boolean>] -MatchValue <String[]> [-Transform <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e403a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e403a-105">DESCRIPTION</span></span>
<span data-ttu-id="e403a-106">A **New-AzApplicationGatewayFirewallCondition** létrehoz egy egyeztetési feltételt a tűzfal egyéni szabályához.</span><span class="sxs-lookup"><span data-stu-id="e403a-106">The **New-AzApplicationGatewayFirewallCondition** creates a match condition for firewall custom rule.</span></span>

## <span data-ttu-id="e403a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e403a-107">EXAMPLES</span></span>

### <span data-ttu-id="e403a-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e403a-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzureRmApplicationGatewayFirewallConditon -MatchVariables $variable -Operator Contains -NegationConditon false -Transforms Lowercase, Trim -MatchValues abc, cde
```

<span data-ttu-id="e403a-109">A parancs új egyeztetési feltételt hoz létre a $variableban definiált egyezési változóval, az operátor tartalmaz és tagadási feltételt tartalmaz, a Transfroms, például a kisbetűs és a kimetszet, a hol. van érték az ABC és a CDE.</span><span class="sxs-lookup"><span data-stu-id="e403a-109">The command creates a new match condition using the match variable defined in the $variable, the operator is Contains and negation condition is false, Transfroms including lowercase and trim, the match value is abc and cde.</span></span> <span data-ttu-id="e403a-110">A program az új egyezési feltételt $condition menti.</span><span class="sxs-lookup"><span data-stu-id="e403a-110">The new match condition is saved in $condition.</span></span>

## <span data-ttu-id="e403a-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e403a-111">PARAMETERS</span></span>

### <span data-ttu-id="e403a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e403a-112">-DefaultProfile</span></span>
<span data-ttu-id="e403a-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e403a-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e403a-114">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="e403a-114">-MatchValue</span></span>
<span data-ttu-id="e403a-115">Az érték egyeztetése</span><span class="sxs-lookup"><span data-stu-id="e403a-115">Match value.</span></span>

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

### <span data-ttu-id="e403a-116">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="e403a-116">-MatchVariable</span></span>
<span data-ttu-id="e403a-117">A egyezési változók listája.</span><span class="sxs-lookup"><span data-stu-id="e403a-117">List of match variables.</span></span>

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

### <span data-ttu-id="e403a-118">-NegationCondition</span><span class="sxs-lookup"><span data-stu-id="e403a-118">-NegationCondition</span></span>
<span data-ttu-id="e403a-119">Ez a cikk azt ismerteti, hogy a feltétel nincs-e megtagadva.</span><span class="sxs-lookup"><span data-stu-id="e403a-119">Describes if this is negate condition or not.</span></span>

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

### <span data-ttu-id="e403a-120">-Operátor</span><span class="sxs-lookup"><span data-stu-id="e403a-120">-Operator</span></span>
<span data-ttu-id="e403a-121">A megfelelő operátort ismerteti.</span><span class="sxs-lookup"><span data-stu-id="e403a-121">Describes operator to be matched.</span></span>

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

### <span data-ttu-id="e403a-122">-Transform</span><span class="sxs-lookup"><span data-stu-id="e403a-122">-Transform</span></span>
<span data-ttu-id="e403a-123">Az átalakítások listája.</span><span class="sxs-lookup"><span data-stu-id="e403a-123">List of transforms.</span></span>

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

### <span data-ttu-id="e403a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e403a-124">CommonParameters</span></span>
<span data-ttu-id="e403a-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e403a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e403a-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e403a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e403a-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e403a-127">INPUTS</span></span>

### <span data-ttu-id="e403a-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="e403a-128">None</span></span>

## <span data-ttu-id="e403a-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e403a-129">OUTPUTS</span></span>

### <span data-ttu-id="e403a-130">Microsoft. Azure. commands. Network. models. PSApplicationGatewayFirewallCondition</span><span class="sxs-lookup"><span data-stu-id="e403a-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCondition</span></span>

## <span data-ttu-id="e403a-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e403a-131">NOTES</span></span>

## <span data-ttu-id="e403a-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e403a-132">RELATED LINKS</span></span>
