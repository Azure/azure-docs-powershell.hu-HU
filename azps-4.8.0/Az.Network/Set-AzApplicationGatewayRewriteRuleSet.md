---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 45d7fdf6a276e98ce0aca2c2a0db6989e062e42c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024554"
---
# <span data-ttu-id="adcf4-101">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="adcf4-101">Set-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="adcf4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="adcf4-102">SYNOPSIS</span></span>
<span data-ttu-id="adcf4-103">Módosítja az alkalmazás-átjárók átírási szabályát.</span><span class="sxs-lookup"><span data-stu-id="adcf4-103">Modifies a rewrite rule set for an application gateway.</span></span>

## <span data-ttu-id="adcf4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="adcf4-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayRewriteRuleSet -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="adcf4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="adcf4-105">DESCRIPTION</span></span>
<span data-ttu-id="adcf4-106">A **set-AzApplicationGatewayRewriteRuleSet** parancsmag módosítja a kérések útválasztási szabályát.</span><span class="sxs-lookup"><span data-stu-id="adcf4-106">The **Set-AzApplicationGatewayRewriteRuleSet** cmdlet modifies a request routing rule.</span></span>

## <span data-ttu-id="adcf4-107">Példák</span><span class="sxs-lookup"><span data-stu-id="adcf4-107">EXAMPLES</span></span>

### <span data-ttu-id="adcf4-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="adcf4-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "ruleset1" -RewriteRule $rule
```

<span data-ttu-id="adcf4-109">Az első parancs a ApplicationGateway01 nevű alkalmazás-átjárót kapja meg, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="adcf4-109">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="adcf4-110">A második parancs a $rule változóban megadott átírási szabályok használatához módosította az alkalmazás átjárójának átírási szabályát.</span><span class="sxs-lookup"><span data-stu-id="adcf4-110">The second command modifies the rewrite rule set for the application gateway to use rewrite rules specified in the $rule variable.</span></span>

## <span data-ttu-id="adcf4-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="adcf4-111">PARAMETERS</span></span>

### <span data-ttu-id="adcf4-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="adcf4-112">-ApplicationGateway</span></span>
<span data-ttu-id="adcf4-113">A applicationGateway</span><span class="sxs-lookup"><span data-stu-id="adcf4-113">The applicationGateway</span></span>

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

### <span data-ttu-id="adcf4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adcf4-114">-DefaultProfile</span></span>
<span data-ttu-id="adcf4-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="adcf4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="adcf4-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="adcf4-116">-Name</span></span>
<span data-ttu-id="adcf4-117">A RewriteRuleSet neve</span><span class="sxs-lookup"><span data-stu-id="adcf4-117">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="adcf4-118">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="adcf4-118">-RewriteRule</span></span>
<span data-ttu-id="adcf4-119">Az átírási szabályok listája</span><span class="sxs-lookup"><span data-stu-id="adcf4-119">List of rewrite rules</span></span>

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

### <span data-ttu-id="adcf4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adcf4-120">CommonParameters</span></span>
<span data-ttu-id="adcf4-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="adcf4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adcf4-122">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="adcf4-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adcf4-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="adcf4-123">INPUTS</span></span>

### <span data-ttu-id="adcf4-124">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="adcf4-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="adcf4-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="adcf4-125">OUTPUTS</span></span>

### <span data-ttu-id="adcf4-126">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="adcf4-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="adcf4-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="adcf4-127">NOTES</span></span>

## <span data-ttu-id="adcf4-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="adcf4-128">RELATED LINKS</span></span>

[<span data-ttu-id="adcf4-129">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="adcf4-129">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="adcf4-130">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="adcf4-130">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="adcf4-131">Új – AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="adcf4-131">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="adcf4-132">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="adcf4-132">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="adcf4-133">Új – AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="adcf4-133">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="adcf4-134">Új – AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="adcf4-134">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="adcf4-135">Új – AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="adcf4-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
