---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriterule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRule.md
ms.openlocfilehash: 5eaa5cdc8b00fa13d9fc0c06821b664f1afc2a65
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302767"
---
# <span data-ttu-id="62bb4-101">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="62bb4-101">New-AzApplicationGatewayRewriteRule</span></span>

## <span data-ttu-id="62bb4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="62bb4-102">SYNOPSIS</span></span>
<span data-ttu-id="62bb4-103">Újraírási szabályt hoz létre egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="62bb4-103">Creates a rewrite rule for an application gateway.</span></span>

## <span data-ttu-id="62bb4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="62bb4-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRule -Name <String> -ActionSet <PSApplicationGatewayRewriteRuleActionSet>
 [-RuleSequence <Int32>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62bb4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="62bb4-105">DESCRIPTION</span></span>
<span data-ttu-id="62bb4-106">**A New-AzApplicationGatewayRewriteRule** parancsmag átírási szabályt hoz létre az Azure-alkalmazás átjárója számára.</span><span class="sxs-lookup"><span data-stu-id="62bb4-106">**The New-AzApplicationGatewayRewriteRule** cmdlet creates a rewrite rule for an Azure application gateway.</span></span>

## <span data-ttu-id="62bb4-107">Példák</span><span class="sxs-lookup"><span data-stu-id="62bb4-107">EXAMPLES</span></span>

### <span data-ttu-id="62bb4-108">Példa 1: átírási szabály létrehozása az alkalmazás-átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="62bb4-108">Example 1 : Create a rewrite rule for an application gateway</span></span>
```powershell
PS C:\> $rule = New-AzApplicationGatewayRewriteRule -Name rule1 -ActionSet $action -RuleSequence 101 -Condition $condition
```

<span data-ttu-id="62bb4-109">Ez a parancs létrehoz egy Szabály1 nevű átírási szabályt, és az eredményt az $rule nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="62bb4-109">This command creates a rewrite rule named rule1 and stores the result in the variable named $rule.</span></span>

## <span data-ttu-id="62bb4-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="62bb4-110">PARAMETERS</span></span>

### <span data-ttu-id="62bb4-111">-ActionSet</span><span class="sxs-lookup"><span data-stu-id="62bb4-111">-ActionSet</span></span>
<span data-ttu-id="62bb4-112">Az átírási szabály ActionSet</span><span class="sxs-lookup"><span data-stu-id="62bb4-112">ActionSet of the rewrite rule</span></span>

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

### <span data-ttu-id="62bb4-113">-Feltétel</span><span class="sxs-lookup"><span data-stu-id="62bb4-113">-Condition</span></span>
<span data-ttu-id="62bb4-114">Az Újraírási szabály feltétele a végrehajtáshoz</span><span class="sxs-lookup"><span data-stu-id="62bb4-114">Condition for the rewrite rule to execute</span></span>

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

### <span data-ttu-id="62bb4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62bb4-115">-DefaultProfile</span></span>
<span data-ttu-id="62bb4-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="62bb4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62bb4-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="62bb4-117">-Name</span></span>
<span data-ttu-id="62bb4-118">A RewriteRule neve</span><span class="sxs-lookup"><span data-stu-id="62bb4-118">The name of the RewriteRule</span></span>

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

### <span data-ttu-id="62bb4-119">-RuleSequence</span><span class="sxs-lookup"><span data-stu-id="62bb4-119">-RuleSequence</span></span>
<span data-ttu-id="62bb4-120">Az Újraírási szabály elrendelése az Újraírási szabály halmazában</span><span class="sxs-lookup"><span data-stu-id="62bb4-120">The rule ordering of this rewrite rule in the rewrite rule set</span></span>

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

### <span data-ttu-id="62bb4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62bb4-121">CommonParameters</span></span>
<span data-ttu-id="62bb4-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="62bb4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62bb4-123">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62bb4-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62bb4-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="62bb4-124">INPUTS</span></span>

### <span data-ttu-id="62bb4-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="62bb4-125">None</span></span>

## <span data-ttu-id="62bb4-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="62bb4-126">OUTPUTS</span></span>

### <span data-ttu-id="62bb4-127">Microsoft. Azure. commands. Network. models. PSApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="62bb4-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule</span></span>

## <span data-ttu-id="62bb4-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="62bb4-128">NOTES</span></span>

## <span data-ttu-id="62bb4-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="62bb4-129">RELATED LINKS</span></span>

[<span data-ttu-id="62bb4-130">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="62bb4-130">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="62bb4-131">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="62bb4-131">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="62bb4-132">Új – AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="62bb4-132">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="62bb4-133">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="62bb4-133">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="62bb4-134">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="62bb4-134">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="62bb4-135">Új – AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="62bb4-135">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="62bb4-136">Új – AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="62bb4-136">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
