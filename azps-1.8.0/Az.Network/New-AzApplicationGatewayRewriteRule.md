---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriterule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRule.md
ms.openlocfilehash: 9fdbf6f7cd88774c2d14d079201993f6a324ace5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670390"
---
# <span data-ttu-id="670e5-101">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="670e5-101">New-AzApplicationGatewayRewriteRule</span></span>

## <span data-ttu-id="670e5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="670e5-102">SYNOPSIS</span></span>
<span data-ttu-id="670e5-103">Újraírási szabályt hoz létre egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="670e5-103">Creates a rewrite rule for an application gateway.</span></span>

## <span data-ttu-id="670e5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="670e5-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRule -Name <String> -ActionSet <PSApplicationGatewayRewriteRuleActionSet>
 [-RuleSequence <Int32>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="670e5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="670e5-105">DESCRIPTION</span></span>
<span data-ttu-id="670e5-106">**A New-AzApplicationGatewayRewriteRule** parancsmag átírási szabályt hoz létre az Azure-alkalmazás átjárója számára.</span><span class="sxs-lookup"><span data-stu-id="670e5-106">**The New-AzApplicationGatewayRewriteRule** cmdlet creates a rewrite rule for an Azure application gateway.</span></span>

## <span data-ttu-id="670e5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="670e5-107">EXAMPLES</span></span>

### <span data-ttu-id="670e5-108">Példa 1: átírási szabály létrehozása az alkalmazás-átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="670e5-108">Example 1 : Create a rewrite rule for an application gateway</span></span>
```powershell
PS C:\> $rule = New-AzApplicationGatewayRewriteRule -Name rule1 -ActionSet $action -RuleSequence 101 -Condition $condition
```

<span data-ttu-id="670e5-109">Ez a parancs létrehoz egy Szabály1 nevű átírási szabályt, és az eredményt az $rule nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="670e5-109">This command creates a rewrite rule named rule1 and stores the result in the variable named $rule.</span></span>

## <span data-ttu-id="670e5-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="670e5-110">PARAMETERS</span></span>

### <span data-ttu-id="670e5-111">-ActionSet</span><span class="sxs-lookup"><span data-stu-id="670e5-111">-ActionSet</span></span>
<span data-ttu-id="670e5-112">Az átírási szabály ActionSet</span><span class="sxs-lookup"><span data-stu-id="670e5-112">ActionSet of the rewrite rule</span></span>

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

### <span data-ttu-id="670e5-113">-Feltétel</span><span class="sxs-lookup"><span data-stu-id="670e5-113">-Condition</span></span>
<span data-ttu-id="670e5-114">Az Újraírási szabály feltétele a végrehajtáshoz</span><span class="sxs-lookup"><span data-stu-id="670e5-114">Condition for the rewrite rule to execute</span></span>

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

### <span data-ttu-id="670e5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="670e5-115">-DefaultProfile</span></span>
<span data-ttu-id="670e5-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="670e5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="670e5-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="670e5-117">-Name</span></span>
<span data-ttu-id="670e5-118">A RewriteRule neve</span><span class="sxs-lookup"><span data-stu-id="670e5-118">The name of the RewriteRule</span></span>

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

### <span data-ttu-id="670e5-119">-RuleSequence</span><span class="sxs-lookup"><span data-stu-id="670e5-119">-RuleSequence</span></span>
<span data-ttu-id="670e5-120">Az Újraírási szabály elrendelése az Újraírási szabály halmazában</span><span class="sxs-lookup"><span data-stu-id="670e5-120">The rule ordering of this rewrite rule in the rewrite rule set</span></span>

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

### <span data-ttu-id="670e5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="670e5-121">CommonParameters</span></span>
<span data-ttu-id="670e5-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="670e5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="670e5-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="670e5-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="670e5-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="670e5-124">INPUTS</span></span>

### <span data-ttu-id="670e5-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="670e5-125">None</span></span>

## <span data-ttu-id="670e5-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="670e5-126">OUTPUTS</span></span>

### <span data-ttu-id="670e5-127">Microsoft. Azure. commands. Network. models. PSApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="670e5-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule</span></span>

## <span data-ttu-id="670e5-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="670e5-128">NOTES</span></span>

## <span data-ttu-id="670e5-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="670e5-129">RELATED LINKS</span></span>

[<span data-ttu-id="670e5-130">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="670e5-130">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="670e5-131">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="670e5-131">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="670e5-132">Új – AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="670e5-132">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="670e5-133">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="670e5-133">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="670e5-134">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="670e5-134">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="670e5-135">Új – AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="670e5-135">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="670e5-136">Új – AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="670e5-136">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
