---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 01f1dc89257088c053cdd6003384c31c708d6b04
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303644"
---
# <span data-ttu-id="9e568-101">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9e568-101">Remove-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="9e568-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9e568-102">SYNOPSIS</span></span>
<span data-ttu-id="9e568-103">Egy alkalmazás-átjárótól származó átírási szabály eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="9e568-103">Removes a rewrite rule set from an application gateway.</span></span>

## <span data-ttu-id="9e568-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9e568-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRewriteRuleSet -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e568-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9e568-105">DESCRIPTION</span></span>
<span data-ttu-id="9e568-106">A **Remove-AzApplicationGatewayRewriteRuleSet** parancsmag eltávolítja az Azure Application Gateway-ből származó átírási szabályt.</span><span class="sxs-lookup"><span data-stu-id="9e568-106">The **Remove-AzApplicationGatewayRewriteRuleSet** cmdlet removes a rewrite rule set from an Azure application gateway.</span></span>

## <span data-ttu-id="9e568-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9e568-107">EXAMPLES</span></span>

### <span data-ttu-id="9e568-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9e568-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "RuleSet02"
```

<span data-ttu-id="9e568-109">Az első parancs beolvassa az Application Gatewayt, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="9e568-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="9e568-110">A második parancs eltávolítja a RuleSet02 nevű, az $AppGw-ban tárolt alkalmazásobjektum-készlet átírási szabályát.</span><span class="sxs-lookup"><span data-stu-id="9e568-110">The second command removes the rewrite rule set named RuleSet02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="9e568-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9e568-111">PARAMETERS</span></span>

### <span data-ttu-id="9e568-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9e568-112">-ApplicationGateway</span></span>
<span data-ttu-id="9e568-113">A applicationGateway</span><span class="sxs-lookup"><span data-stu-id="9e568-113">The applicationGateway</span></span>

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

### <span data-ttu-id="9e568-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e568-114">-DefaultProfile</span></span>
<span data-ttu-id="9e568-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9e568-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e568-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9e568-116">-Name</span></span>
<span data-ttu-id="9e568-117">Az alkalmazás-átjáró RewriteRuleSet neve</span><span class="sxs-lookup"><span data-stu-id="9e568-117">The name of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="9e568-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e568-118">CommonParameters</span></span>
<span data-ttu-id="9e568-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9e568-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e568-120">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e568-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e568-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9e568-121">INPUTS</span></span>

### <span data-ttu-id="9e568-122">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9e568-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9e568-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9e568-123">OUTPUTS</span></span>

### <span data-ttu-id="9e568-124">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9e568-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9e568-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9e568-125">NOTES</span></span>

## <span data-ttu-id="9e568-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9e568-126">RELATED LINKS</span></span>

[<span data-ttu-id="9e568-127">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9e568-127">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="9e568-128">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9e568-128">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="9e568-129">Új – AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9e568-129">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="9e568-130">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9e568-130">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="9e568-131">Új – AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="9e568-131">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="9e568-132">Új – AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="9e568-132">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="9e568-133">Új – AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="9e568-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
