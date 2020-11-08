---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 6e45f0bc0eaab8316d0534e1f73a1543175e1144
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024665"
---
# <span data-ttu-id="8e064-101">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8e064-101">Add-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="8e064-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8e064-102">SYNOPSIS</span></span>
<span data-ttu-id="8e064-103">Egy alkalmazás-átjáróhoz tartozó Újraírási szabály hozzáadása</span><span class="sxs-lookup"><span data-stu-id="8e064-103">Adds a rewrite rule set to an application gateway.</span></span>

## <span data-ttu-id="8e064-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8e064-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayRewriteRuleSet -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e064-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8e064-105">DESCRIPTION</span></span>
<span data-ttu-id="8e064-106">Az **Add-AzApplicationGatewayRewriteRuleSet** parancsmag átírási szabályt ad hozzá egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="8e064-106">The **Add-AzApplicationGatewayRewriteRuleSet** cmdlet adds a rewrite rule set to an application gateway.</span></span>

## <span data-ttu-id="8e064-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8e064-107">EXAMPLES</span></span>

### <span data-ttu-id="8e064-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8e064-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "ruleset1" -RewriteRule $rule
```

<span data-ttu-id="8e064-109">Az első parancs beolvassa az Application Gatewayt, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="8e064-109">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="8e064-110">A második parancs hozzáadja az átírás szabályt az alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="8e064-110">The second command adds the rewrite rule set to the application gateway.</span></span>

## <span data-ttu-id="8e064-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8e064-111">PARAMETERS</span></span>

### <span data-ttu-id="8e064-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8e064-112">-ApplicationGateway</span></span>
<span data-ttu-id="8e064-113">A applicationGateway</span><span class="sxs-lookup"><span data-stu-id="8e064-113">The applicationGateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e064-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e064-114">-DefaultProfile</span></span>
<span data-ttu-id="8e064-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8e064-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e064-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8e064-116">-Name</span></span>
<span data-ttu-id="8e064-117">A RewriteRuleSet neve</span><span class="sxs-lookup"><span data-stu-id="8e064-117">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="8e064-118">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="8e064-118">-RewriteRule</span></span>
<span data-ttu-id="8e064-119">Az átírási szabályok listája</span><span class="sxs-lookup"><span data-stu-id="8e064-119">List of rewrite rules</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e064-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e064-120">CommonParameters</span></span>
<span data-ttu-id="8e064-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8e064-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e064-122">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e064-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e064-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e064-123">INPUTS</span></span>

### <span data-ttu-id="8e064-124">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8e064-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8e064-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e064-125">OUTPUTS</span></span>

### <span data-ttu-id="8e064-126">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8e064-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8e064-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8e064-127">NOTES</span></span>

## <span data-ttu-id="8e064-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8e064-128">RELATED LINKS</span></span>

[<span data-ttu-id="8e064-129">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8e064-129">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="8e064-130">Új – AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8e064-130">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="8e064-131">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8e064-131">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="8e064-132">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8e064-132">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="8e064-133">Új – AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="8e064-133">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="8e064-134">Új – AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="8e064-134">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="8e064-135">Új – AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="8e064-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
