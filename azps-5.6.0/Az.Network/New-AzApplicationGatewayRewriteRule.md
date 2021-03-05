---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayrewriterule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRule.md
ms.openlocfilehash: a69f5a3a1da8ec2ac8937793051f0361bf5e0681
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011894"
---
# <span data-ttu-id="6a515-101">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="6a515-101">New-AzApplicationGatewayRewriteRule</span></span>

## <span data-ttu-id="6a515-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a515-102">SYNOPSIS</span></span>
<span data-ttu-id="6a515-103">Újraírási szabályt hoz létre egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="6a515-103">Creates a rewrite rule for an application gateway.</span></span>

## <span data-ttu-id="6a515-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6a515-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRule -Name <String> -ActionSet <PSApplicationGatewayRewriteRuleActionSet>
 [-RuleSequence <Int32>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a515-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6a515-105">DESCRIPTION</span></span>
<span data-ttu-id="6a515-106">**A New-AzApplicationGatewayRewriteRule parancsmag** létrehoz egy újraírási szabályt egy Azure-alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="6a515-106">**The New-AzApplicationGatewayRewriteRule** cmdlet creates a rewrite rule for an Azure application gateway.</span></span>

## <span data-ttu-id="6a515-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6a515-107">EXAMPLES</span></span>

### <span data-ttu-id="6a515-108">1. példa: Újraírási szabály létrehozása alkalmazás-átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="6a515-108">Example 1 : Create a rewrite rule for an application gateway</span></span>
```powershell
PS C:\> $rule = New-AzApplicationGatewayRewriteRule -Name rule1 -ActionSet $action -RuleSequence 101 -Condition $condition
```

<span data-ttu-id="6a515-109">Ez a parancs létrehoz egy szabály1 nevű újraírási szabályt, és az eredményt a következő nevű változóban $rule.</span><span class="sxs-lookup"><span data-stu-id="6a515-109">This command creates a rewrite rule named rule1 and stores the result in the variable named $rule.</span></span>

## <span data-ttu-id="6a515-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6a515-110">PARAMETERS</span></span>

### <span data-ttu-id="6a515-111">-ActionSet</span><span class="sxs-lookup"><span data-stu-id="6a515-111">-ActionSet</span></span>
<span data-ttu-id="6a515-112">Az átírási szabály ActionSet műveletkészlete</span><span class="sxs-lookup"><span data-stu-id="6a515-112">ActionSet of the rewrite rule</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleActionSet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a515-113">-Feltétel</span><span class="sxs-lookup"><span data-stu-id="6a515-113">-Condition</span></span>
<span data-ttu-id="6a515-114">Az újraírási szabály végrehajtásához szükséges feltétel</span><span class="sxs-lookup"><span data-stu-id="6a515-114">Condition for the rewrite rule to execute</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a515-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a515-115">-DefaultProfile</span></span>
<span data-ttu-id="6a515-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6a515-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a515-117">-Name</span><span class="sxs-lookup"><span data-stu-id="6a515-117">-Name</span></span>
<span data-ttu-id="6a515-118">A RewriteRule neve</span><span class="sxs-lookup"><span data-stu-id="6a515-118">The name of the RewriteRule</span></span>

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

### <span data-ttu-id="6a515-119">-RuleSequence</span><span class="sxs-lookup"><span data-stu-id="6a515-119">-RuleSequence</span></span>
<span data-ttu-id="6a515-120">Az újraírási szabály szabályrendje az újraírási szabálykészletben</span><span class="sxs-lookup"><span data-stu-id="6a515-120">The rule ordering of this rewrite rule in the rewrite rule set</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a515-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a515-121">CommonParameters</span></span>
<span data-ttu-id="6a515-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a515-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a515-123">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a515-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a515-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6a515-124">INPUTS</span></span>

### <span data-ttu-id="6a515-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="6a515-125">None</span></span>

## <span data-ttu-id="6a515-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6a515-126">OUTPUTS</span></span>

### <span data-ttu-id="6a515-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="6a515-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule</span></span>

## <span data-ttu-id="6a515-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6a515-128">NOTES</span></span>

## <span data-ttu-id="6a515-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6a515-129">RELATED LINKS</span></span>

[<span data-ttu-id="6a515-130">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6a515-130">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="6a515-131">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6a515-131">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="6a515-132">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6a515-132">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="6a515-133">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6a515-133">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="6a515-134">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6a515-134">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="6a515-135">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="6a515-135">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="6a515-136">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="6a515-136">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
